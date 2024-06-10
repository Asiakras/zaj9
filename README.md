# Wtyczka do porgramu QGIS - projekt na zajecia Informatyka Geodezyjna sem. 4

## Wymagania systemowe:
  - system Windows 10
  - program QGIS (w wersji minimum 3.3X)
  - python 3.X
  - posiadanie bibliotek:
    - qgis.PyQt
    - qgis.core
    - qgis.utils
    - numpy
    - os


## Funkcje wtyczki:

  1. Liczenie ilości obiektów na wybranej warstiwe
     Funkcja liczy obiekty na wybranej warstwie za pomocą komeny "featureCount" i pokazuje wynik.
  2. Liczenie różnic wysokości pomiędzy dwoma wybranymi punktami
     Na pdostawie danych zczytanych z geometrii wybranych punktów a dokładniej własności "wysokosc" funkcja oblicza różnice przewyższeń pomiędzy punktami. Wynik może się pojawić dodatni lub ujemny w zależoności od wybranych puntów i jego jednostkami są metry. Wynik jest podawany z dokładnością 3 miejsc po przecinku.
  3. Pokazanie współrzędnych wybranych punktów
     Funkcja zczytuje współrzędne zaznaczonych punktów z pliku użytego w programie QGIS i pokazuje ich wartości XYZ w oknie wtyczki. 
  4. Liczenie pola powierzchni pomiędzy zaznaczonymi punktami
     Funkcja ściąga wartości X i Y zaznaczonych punktów. Następnie na podstawie tych współrzędych, program policzy pole powierzchni zawarte między nimi. Obliczneia są robione metodą Gaussa i jednostkami wyniku są metry kwadratowe. Wynik jest podawany z dokładnością 3 miejsc po przecinku.   

    
## Sposób użycia wtyczki:
  1. Pobrać wtyczkę i umieścić ją w folderze z innymi wtyczkami, przykładowa ścieżka do folderu:                          "C:\Users\Student\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins"                             a następnie w programie QGIS załadować wtyczkę.
  2. Następnie wczytać plik z danymi w naszym przypdaku danymi są punkty. 
  3. Po wczytaniu sieci punktów zaznaczyć w programie QGIS 2 lub więcej punktów.
  5. W oknie wtyczki wybrać odpowiednią wartswę na której leżą wybrane punkty
  6. By obliczyć przewyższenie między dwoma punktami trzeba kliknąć przycisk "obliczanie" obok etykiety "przewyższenie"
  7. Aby obliczzyć pole miedzy ilością punktów większą niż dwa trzeba kliknąć przycisk "oblicz" obok etykiety pole
  8. Opcjonalnie można wyświetlić liczbę obietków znajdujących na aktualnej warstwie przyciskiem "zlicz" oraz wyświetlić współrzędne zaznaczonych punktów klikając przycisk "pokaż" 
