#### Diagram

:[Diagram](diagram.puml)

#### Przypadki użycia

##### UC2001 Zgłoszenie błędów danych

**nazwa:** Zgłoszenie błędów danych

**aktorzy:** Klient/Użytkownik danych, System

**opis:**  
    System umożliwia użytkownikowi zgłoszenie błędu w danych. Zgłoszenie jest rejestrowane w celu późniejszej weryfikacji przez administratora lub dedykowany zespół ds. jakości danych.

**kroki:**
1. **Klient/Użytkownik danych** wybiera opcję "Zgłoś błąd danych".
2. **System** wyświetla formularz zgłoszenia błędu.
3. **Klient/Użytkownik danych** wypełnia formularz, podając opis błędu oraz ewentualne szczegóły.
4. **Klient/Użytkownik danych** zatwierdza przesłanie zgłoszenia.
5. **System** rejestruje zgłoszenie błędu i wyświetla komunikat potwierdzający.

---

##### UC2002 Zatwierdzenie zgłoszonych błędów danych

**nazwa:** Zatwierdzenie zgłoszonych błędów danych

**aktorzy:** Administrator systemu, System

**opis:**  
    Administrator weryfikuje zgłoszone błędy danych i zatwierdza je, jeśli zgłoszenie jest uzasadnione, co umożliwia dalsze działania naprawcze.

**kroki:**
1. **Administrator systemu** loguje się do systemu i przechodzi do sekcji zgłoszeń błędów.
2. **System** prezentuje listę oczekujących zgłoszeń.
3. **Administrator systemu** wybiera zgłoszenie do weryfikacji.
4. **System** wyświetla szczegóły zgłoszenia.
5. **Administrator systemu** zatwierdza zgłoszenie.
6. **System** rejestruje zatwierdzenie i aktualizuje status zgłoszenia.

---

##### UC2003 Odrzucenie zgłoszenia i powiadomienie użytkownika

**nazwa:** Odrzucenie zgłoszenia błędu i powiadomienie użytkownika

**aktorzy:** Administrator systemu, System

**opis:**  
    W przypadku uznania zgłoszenia za nieuzasadnione, administrator odrzuca zgłoszenie i powiadamia użytkownika o przyczynach odrzucenia.

**kroki:**
1. **Administrator systemu** przegląda zgłoszenie błędu.
2. **System** prezentuje szczegóły zgłoszenia.
3. **Administrator systemu** wybiera opcję "Odrzuć zgłoszenie".
4. **System** rejestruje decyzję o odrzuceniu.
5. **System** generuje powiadomienie z uzasadnieniem decyzji.
6. **System** wysyła powiadomienie do Klienta/Użytkownika danych.

**alt 1 – Problem z powiadomieniem:**  
1. **System** wykrywa problem z wysyłką powiadomienia (np. niepoprawny adres email).  
2. **System** loguje błąd i informuje administratora o problemie.

---

##### UC2004 Wykrywanie anomalii

**nazwa:** Wykrywanie anomalii w danych

**aktorzy:** System

**opis:**  
    System automatycznie analizuje dane, identyfikując nieprawidłowości lub odstępstwa od normy przy użyciu algorytmów wykrywania anomalii.

**kroki:**
1. **System** okresowo analizuje dane w zbiorach.
2. **System** stosuje algorytmy wykrywania anomalii.
3. **System** rejestruje zdarzenie w przypadku wykrycia nieprawidłowości.
4. **System** generuje alert o wykrytej anomalii.

**alt 1 – Brak wykrycia anomalii:**  
1. **System** nie generuje alertu, gdy dane mieszczą się w ustalonych normach.

**alt 2 – Błąd algorytmu wykrywania:**  
1. **System** loguje błąd w algorytmie i informuje administratora o konieczności interwencji.

---

##### UC2005 Wyświetlanie wykrytych anomalii

**nazwa:** Wyświetlanie wykrytych anomalii

**aktorzy:** Klient/Użytkownik danych, System

**opis:**  
    System umożliwia użytkownikowi przeglądanie listy wykrytych anomalii, prezentując szczegóły takie jak rodzaj anomalii, data wykrycia oraz miejsce wystąpienia.

**kroki:**
1. **Klient/Użytkownik danych** wybiera opcję "Wyświetl anomalie".
2. **System** pobiera listę wykrytych anomalii z bazy danych.
3. **System** generuje czytelną listę z kluczowymi informacjami.
4. **System** wyświetla listę wykrytych anomalii.

**alt 1 – Brak wykrytych anomalii:**  
1. **System** wyświetla komunikat informujący o braku wykrytych anomalii.

---

##### UC2006 Walidacja istnienia zbiorów danych

**nazwa:** Walidacja istnienia zbiorów danych

**aktorzy:** System

**opis:**  
    System sprawdza, czy wymagane zbiory danych są dostępne przed rozpoczęciem operacji przetwarzania lub analizy.

**kroki:**
1. **System** otrzymuje zapytanie dotyczące operacji na danych.
2. **System** przeszukuje bazę danych w celu potwierdzenia istnienia wymaganych zbiorów.
3. **System** kontynuuje operację, jeśli wszystkie zbiory są dostępne.
4. **System** przerywa operację i loguje błąd, jeśli brak jest jednego z wymaganych zbiorów.

**alt 1 – Brak wymaganego zbioru:**  
1. **System** wyświetla komunikat błędu informujący o braku niezbędnego zbioru danych.

---
