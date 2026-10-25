# ADM – RAPORT Z WYBORU BAZY DANYCH

**Tytuł projektu:** Rozpoznawanie aktywności człowieka na podstawie danych z akcelerometru smartfona

**Wybrana baza danych:** WISDM – Activity Prediction v1.1

## 1. Skład grupy i podział zadań

* **Maciej Morawiak** – lider grupy, przygotowanie raportu.
* **Jakub Maciocha** – przetwarzanie danych i wydzielanie obiektów.
* **Szymon Mruszczyk** – obliczanie cech.
* **Jakub Marecki** – analiza statystyczna danych.

## 2. Porównanie baz danych i uzasadnienie wyboru

Na początku porównaliśmy dwie bazy danych, które dotyczą rozpoznawania aktywności człowieka na podstawie danych zbieranych przez smartfony.

Pierwsza z nich to **UCI HAR**, która zawiera dane z akcelerometru i żyroskopu. Zostały one zebrane od 30 osób wykonujących sześć różnych aktywności. Baza zawiera już przetworzone dane i 561 wyznaczonych cech. Jest również podzielona na zbiór treningowy i testowy, co ułatwia wykorzystanie jej w uczeniu maszynowym.

Druga baza to **WISDM**, zawierająca dane z akcelerometru smartfona zebrane od 36 osób. Uczestnicy wykonywali sześć aktywności, między innymi chodzenie, bieganie, siedzenie i poruszanie się po schodach. Baza udostępnia zarówno surowe pomiary, jak i dane przetworzone.

**Do naszego projektu wybraliśmy bazę WISDM.**

Głównym powodem jest to, że mamy dostęp do surowych danych z akcelerometru. Dzięki temu możemy sami przygotować dane do analizy, wydzielić odpowiednie fragmenty sygnału i obliczyć interesujące nas cechy.

W przypadku UCI HAR większość tych czynności została już wykonana. Natomiast WISDM daje nam więcej możliwości samodzielnej pracy z danymi, co lepiej pasuje do zadań, które mamy wykonać w ramach projektu.

Dodatkowo możemy porównać, jak zmieniają się odczyty akcelerometru podczas różnych aktywności, np. chodzenia i biegania, oraz sprawdzić, czy na podstawie tych różnic da się określić rodzaj wykonywanego ruchu.

## 3. Opis wybranej bazy danych

WISDM (Wireless Sensor Data Mining) to zbiór danych przygotowany przez zespół badawczy z Fordham University.

Dane zostały zebrane podczas eksperymentu, w którym 36 uczestników wykonywało określone czynności ze smartfonem wyposażonym w akcelerometr. Telefon rejestrował przyspieszenie w trzech osiach: X, Y i Z.

Baza zawiera ponad milion pojedynczych pomiarów. Każdy pomiar ma przypisany identyfikator użytkownika, rodzaj aktywności, czas pomiaru oraz wartości przyspieszenia.

### Rodzaje aktywności

W bazie znajdują się dane dotyczące sześciu aktywności:

1. Walking – chodzenie.
2. Jogging – bieganie.
3. Upstairs – wchodzenie po schodach.
4. Downstairs – schodzenie po schodach.
5. Sitting – siedzenie.
6. Standing – stanie.

Aktywności możemy podzielić na dwie główne grupy:

* **Dynamiczne:** chodzenie, bieganie, wchodzenie i schodzenie po schodach.
* **Statyczne:** siedzenie i stanie.

Taki podział pozwoli nam sprawdzić, jak różnią się wartości przyspieszenia podczas ruchu i spoczynku.

