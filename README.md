# ADM_projekt

Datasety:
 - https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones
 - https://www.cis.fordham.edu/wisdm/dataset.php

# RAPORT – WYBÓR ZBIORU DANYCH I KONSPEKT PROJEKTU

**Kod projektu:** HAR-01 (roboczy)

**Tytuł projektu:** Rozpoznawanie aktywności człowieka na podstawie danych z akcelerometru smartfona z wykorzystaniem metod uczenia maszynowego

**Wybrana baza danych:** WISDM – Activity Prediction v1.1

## 1. Skład grupy i podział zadań

**Członek grupy 1:** [Imię i nazwisko]
Zadania: Pobranie zbioru danych, zapoznanie się z jego strukturą, przygotowanie danych do analizy oraz ich wstępne oczyszczenie.

**Członek grupy 2:** [Imię i nazwisko]
Zadania: Przeprowadzenie analizy eksploracyjnej, przygotowanie wizualizacji oraz porównanie charakterystyki poszczególnych aktywności.

**Członek grupy 3:** [Imię i nazwisko]
Zadania: Przygotowanie i trenowanie modeli uczenia maszynowego, porównanie uzyskanych wyników oraz opracowanie końcowych wniosków.

## 2. Porównanie baz danych i uzasadnienie wyboru

Przed rozpoczęciem projektu przeanalizowaliśmy dwa publicznie dostępne zbiory danych dotyczące rozpoznawania aktywności człowieka na podstawie pomiarów wykonywanych przez smartfony:

* **WISDM (Wireless Sensor Data Mining)** – zbiór danych opracowany przez WISDM Lab na Fordham University.
* **UCI HAR (Human Activity Recognition Using Smartphones)** – zbiór udostępniony w UCI Machine Learning Repository.

Obydwie bazy pozwalają na analizowanie aktywności człowieka oraz budowanie modeli klasyfikacyjnych. Różnią się jednak sposobem przygotowania danych i dostępnymi informacjami.

Baza UCI HAR zawiera pomiary pochodzące z akcelerometru i żyroskopu smartfona. Dane zostały wcześniej przetworzone i opisane za pomocą 561 cech. Zbiór obejmuje 30 uczestników oraz sześć rodzajów aktywności. Jego zaletą jest gotowy podział na dane treningowe i testowe, co ułatwia rozpoczęcie pracy z algorytmami uczenia maszynowego.

Baza WISDM obejmuje dane pochodzące od 36 uczestników wykonujących sześć różnych aktywności. Zawiera zarówno surowe pomiary przyspieszenia w trzech osiach, jak i dane przetworzone, opisane za pomocą 46 atrybutów. W wersji Activity Prediction v1.1 dostępnych jest 1 098 207 surowych pomiarów oraz 5424 rekordy zawierające wyznaczone cechy.

### Uzasadnienie wyboru

**Do realizacji naszego projektu zdecydowaliśmy się wybrać bazę WISDM.**

Głównym powodem jest dostępność surowych danych pomiarowych, które umożliwiają przeprowadzenie pełnego procesu analizy – od przygotowania sygnałów, przez wyznaczanie cech, aż po trenowanie i ocenę modeli uczenia maszynowego.

W przeciwieństwie do UCI HAR nie musimy ograniczać się do korzystania z wcześniej przygotowanych cech. Możemy samodzielnie analizować odczyty akcelerometru i sprawdzić, które właściwości sygnału najlepiej pozwalają rozpoznawać wykonywaną aktywność.

Dodatkową zaletą WISDM jest obecność aktywności jogging, dzięki której możemy porównać charakterystykę zwykłego chodzenia i biegania.

Uważamy, że WISDM daje większe możliwości samodzielnego eksperymentowania z danymi, a tym samym lepiej odpowiada założeniom naszego projektu.

## 3. Charakterystyka wybranej bazy danych

WISDM (Wireless Sensor Data Mining) to zbiór danych opracowany przez laboratorium badawcze zajmujące się analizą informacji pochodzących z urządzeń mobilnych.

Dane zostały zebrane podczas eksperymentu, w którym uczestnicy wykonywali określone czynności, mając przy sobie smartfon wyposażony w akcelerometr. Urządzenie rejestrowało przyspieszenie w trzech osiach: X, Y i Z.

Każdy pomiar został powiązany z konkretnym użytkownikiem, czasem rejestracji oraz rodzajem wykonywanej aktywności.

### Rodzaje aktywności

Zbiór danych obejmuje sześć klas aktywności:

1. **Walking** – chodzenie.
2. **Jogging** – bieganie lub trucht.
3. **Upstairs** – wchodzenie po schodach.
4. **Downstairs** – schodzenie po schodach.
5. **Sitting** – siedzenie.
6. **Standing** – stanie.

Aktywności można dodatkowo podzielić na dwie grupy:

**Aktywności dynamiczne:** chodzenie, bieganie, wchodzenie oraz schodzenie po schodach.

**Aktywności statyczne:** siedzenie i stanie.

### Struktura danych

Baza WISDM udostępnia dwa główne rodzaje danych.

**Dane surowe (Raw Data)** zawierają pojedyncze pomiary akcelerometru. Każdy rekord obejmuje identyfikator użytkownika, nazwę wykonywanej aktywności, znacznik czasu oraz wartości przyspieszenia w osiach X, Y i Z.

**Dane przetworzone (Transformed Data)** zawierają cechy obliczone na podstawie fragmentów sygnału. Są to między innymi informacje statystyczne opisujące wartości przyspieszenia. Dane te można bezpośrednio wykorzystać do budowy modeli klasyfikacyjnych.

Istotną cechą zbioru jest nierównomierna liczba przykładów poszczególnych aktywności. Oznacza to, że podczas trenowania modeli należy uwzględnić różnice w liczebności klas.

## 4. Opis planowanego projektu – konspekt

### Cel projektu

Celem projektu jest opracowanie i porównanie modeli uczenia maszynowego umożliwiających automatyczne rozpoznawanie aktywności człowieka na podstawie pomiarów akcelerometru smartfona.

Chcemy sprawdzić, czy na podstawie danych opisujących ruch urządzenia można prawidłowo określić, czy jego użytkownik chodzi, biega, porusza się po schodach, siedzi lub stoi.

### Planowane etapy realizacji

**Etap 1 – Przygotowanie danych**

W pierwszym etapie pobierzemy zbiór WISDM i zapoznamy się z jego strukturą. Sprawdzimy poprawność danych, występowanie brakujących wartości oraz liczbę obserwacji przypisanych do poszczególnych aktywności.

Następnie przygotujemy dane do dalszej analizy i trenowania modeli.

**Etap 2 – Analiza eksploracyjna i wizualizacja danych**

Przeanalizujemy wartości przyspieszenia rejestrowane podczas wykonywania różnych czynności.

Przygotujemy wykresy przedstawiające zmiany przyspieszenia w czasie, rozkłady wartości pomiarowych oraz różnice między poszczególnymi aktywnościami.

Sprawdzimy również, które aktywności charakteryzują się podobnymi wzorcami ruchu oraz czy można zaobserwować wyraźne różnice między aktywnościami dynamicznymi i statycznymi.

**Etap 3 – Przygotowanie cech**

Na podstawie surowych pomiarów wyznaczymy podstawowe cechy statystyczne, takie jak średnia, odchylenie standardowe, wartości minimalne i maksymalne oraz energia sygnału.

Następnie sprawdzimy, które cechy najlepiej opisują poszczególne aktywności i mogą być najbardziej przydatne w procesie klasyfikacji.

**Etap 4 – Budowa modeli uczenia maszynowego**

W kolejnym etapie wykorzystamy wybrane algorytmy klasyfikacji:

* k-Nearest Neighbors (k-NN),
* Random Forest,
* Logistic Regression.

Każdy model zostanie wytrenowany na przygotowanym zbiorze danych. Następnie porównamy jego skuteczność w rozpoznawaniu sześciu klas aktywności.

**Etap 5 – Ocena wyników**

Do oceny modeli wykorzystamy między innymi dokładność klasyfikacji (accuracy), miarę F1-score oraz macierz pomyłek.

Dane treningowe i testowe podzielimy według uczestników eksperymentu, aby sprawdzić, czy modele potrafią poprawnie klasyfikować aktywności osób, których danych nie wykorzystywano podczas treningu.

Pozwoli to na bardziej wiarygodną ocenę możliwości zastosowania opracowanych modeli.

## 5. Planowane wyniki i wnioski

W ramach projektu chcemy uzyskać odpowiedzi na następujące pytania badawcze:

1. Czy na podstawie danych z akcelerometru smartfona można skutecznie rozpoznawać rodzaj aktywności człowieka?
2. Które aktywności są najłatwiejsze, a które najtrudniejsze do rozpoznania?
3. Który z zastosowanych algorytmów uczenia maszynowego osiąga najlepsze wyniki klasyfikacji?
4. Jakie cechy sygnału mają największe znaczenie podczas rozpoznawania aktywności?
5. Czy model wytrenowany na danych wybranych uczestników będzie skutecznie rozpoznawał aktywności nowych użytkowników?

Efektem końcowym projektu będzie porównanie skuteczności wybranych algorytmów, przygotowanie wizualizacji danych oraz przedstawienie wniosków dotyczących możliwości automatycznego rozpoznawania aktywności człowieka.

Projekt pozwoli również ocenić, w jakim stopniu dane pochodzące z podstawowych czujników urządzeń mobilnych mogą być wykorzystywane w inteligentnych systemach monitorowania aktywności fizycznej.

## 6. Źródła danych

1. WISDM Lab – Dataset, Fordham University:
   https://www.cis.fordham.edu/wisdm/dataset.php

2. UCI Machine Learning Repository – Human Activity Recognition Using Smartphones:
   https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones

3. Kwapisz J. R., Weiss G. M., Moore S. A., *Activity Recognition using Cell Phone Accelerometers*, 2010.
