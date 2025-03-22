#### Diagram

:[Diagram](diagram.puml)

#### Przypadki użycia

##### UC0001 Wyświetlenie zbiorów danych

**nazwa:** Wyświetlanie zbiorów danych

**aktorzy:** Klient/Użytkownik danych, System

**opis:**
    System prezentuje listę wszystkich dostępnych zbiorów danych. Prezentacja powinna być przejrzysta i umożliwiać sortowanie. Użytkownik ma możliwość zapoznawania się z zawartością zbiorów danych.

**kroki:**
1.  **Klient/Użytkownik danych** klika przycisk 'Wyświetl dostępne zbiory'.
2.  **System** pobiera z bazy danych informacje o wszystkich dostępnych zbiorach danych.
3.  **System** generuje przejrzystą listę zbiorów danych.
4.  **System** wyświetla listę zbiorów danych.

**alt 1 Sortowanie zbiorów danych:**
1. **Klient/Użytkownik danych** wybiera opcję sortowania według danego kryterium.
2. **System** sortuje aktualnie wyświetlaną listę zbiorów danych zgodnie z wybranym kryterium.
3. **System** odświeża widok, prezentując posortowaną listę zbiorów danych.

**alt 2 awaria bazy danych:**
1.  **Klient/Użytkownik danych** klika przycisk 'Wyświetl dostępne zbiory'.
2.  **System** próbuje połączyć się z bazą danych w celu pobrania informacji o zbiorach danych.
3.  **System** wykrywa awarię bazy danych (brak połączenia, błędy w odpowiedzi).
4.  **System** wyświetla Klientowi/Użytkownikowi danych komunikat o błędzie informujący o niedostępności danych z powodu awarii bazy danych.

##### UC0002 Wyszukanie zbiorów danych

**nazwa:** Wyszukiwanie zbiorów danych

**aktorzy:** Klient/Użytkownik danych, System

**opis:** System umożliwia użytkownikowi wyszukiwanie konkretnych zbiorów danych na podstawie podanych kryteriów. Wyniki wyszukiwania powinny być czytelne.

**kroki:**
1.  **Klient/Użytkownik danych** wpisuje frazę wyszukiwania lub wybiera kryteria wyszukiwania.
2.  **System** przetwarza zapytanie i przeszukuje dostępne zbiory danych.
3.  **System** generuje listę wyników zgodną z podanymi kryteriami.
4.  **System** wyświetla wyniki wyszukiwania.

**alt 1 Brak wyników wyszukiwania:**
1. **System** nie znajduje zbiorów danych spełniających podane kryteria.
2. **System** wyświetla komunikat informujący o braku wyników oraz sugeruje zmianę kryteriów wyszukiwania.

##### UC0003 Filtrowanie zbiorów danych  

**nazwa:** Filtrowanie zbiorów danych  

**aktorzy:** Klient/Użytkownik danych, System  

**opis:** System umożliwia użytkownikowi zawężenie listy dostępnych zbiorów danych poprzez zastosowanie dodatkowych filtrów.  

**kroki:**  
1. **Klient/Użytkownik danych** wybiera kryteria filtrowania dostępnych zbiorów danych.  
2. **System** przetwarza wybrane kryteria i filtruje dostępne zbiory danych.  
3. **System** generuje i wyświetla zaktualizowaną listę zbiorów danych zgodną z zastosowanymi filtrami.  

**alt 1 Brak wyników po zastosowaniu filtrów:**  
1. **System** nie znajduje zbiorów danych spełniających zastosowane filtry.  
2. **System** wyświetla komunikat o braku wyników i sugeruje zmianę kryteriów filtrowania.  

##### UC0004 Wizualizacja zbioru danych

**nazwa:** Wizualizacja zbiorów danych

**aktorzy:** Klient/Użytkownik danych, System

**opis:**
    System umożliwia użytkownikowi graficzne przedstawienie danych w wybranej formie (np. wykresy, tabele, diagramy) dla lepszej analizy i interpretacji.

**kroki:**
1. **Klient/Użytkownik danych** wybiera zbiór danych do wizualizacji.
2. **System** prezentuje dostępne opcje wizualizacji (np. wykresy słupkowe, liniowe, kołowe).
3. **Klient/Użytkownik danych** wybiera preferowany typ wizualizacji.
4. **System** generuje i wyświetla wizualizację wybranego zbioru danych.

**alt 1 Brak wystarczających danych do wizualizacji:**
1. **System** wykrywa, że wybrany zbiór danych nie zawiera wystarczającej ilości informacji do wygenerowania wizualizacji.
2. **System** wyświetla komunikat informujący o niemożliwości wygenerowania wizualizacji i sugeruje wybór innego zbioru danych lub innej metody prezentacji.

##### UC0005 Prezentacja historii zmian zbioru danych

**nazwa:** Prezentacja historii zmian zbioru danych

**aktorzy:** Klient/Użytkownik danych, System

**opis:**
    System umożliwia użytkownikowi przeglądanie historii zmian wybranego zbioru danych, w tym informacji o modyfikacjach, czasie ich dokonania oraz osobach, które je wykonały.

**kroki:**
1. **Klient/Użytkownik danych** wybiera zbiór danych, dla którego chce zobaczyć historię zmian.
2. **System** pobiera z bazy danych informacje o zmianach dokonanych w wybranym zbiorze.
3. **System** generuje listę zawierającą szczegóły każdej zmiany (np. data, autor, typ zmiany).
4. **System** wyświetla użytkownikowi historię zmian w czytelnej formie.

**alt 1 Brak historii zmian dla zbioru danych:**
1. **System** wykrywa, że dla wybranego zbioru danych nie ma zarejestrowanych zmian.
2. **System** wyświetla komunikat informujący użytkownika o braku historii zmian.

##### UC0006 Dodawanie nowych zbiorów danych

**nazwa:** Dodawanie nowych zbiorów danych

**aktorzy:** Dostawca danych, System

**opis:**
    System umożliwia dostawcy danych dodanie nowego zbioru do systemu, w tym wprowadzenie jego opisu oraz metadanych. Proces dodawania obejmuje walidację danych, która jest realizowana jako osobny przypadek użycia **(include: Walidacja Danych)**.

**kroki:**
1. **Dostawca danych** wybiera opcję dodania nowego zbioru danych.
2. **System** wyświetla formularz do wprowadzenia podstawowych informacji o zbiorze (np. nazwa, opis, kategorie, format pliku).
3. **Dostawca danych** wypełnia formularz i przesyła plik zawierający dane.
4. **System** wykonuje przypadek użycia **Walidacja Danych**.
5. **System** zapisuje nowy zbiór danych w bazie i rejestruje go w katalogu zbiorów.
6. **System** wyświetla komunikat potwierdzający dodanie nowego zbioru danych.

**alt 1 Niepowodzenie walidacji danych:**
1. **System** wykrywa, że przesłany zbiór danych zawiera błędy w ramach przypadku użycia **Walidacja Danych**.
2. **System** wyświetla komunikat o błędach i prosi dostawcę danych o poprawienie i ponowne przesłanie zbioru danych.

##### UC0007 Edycja zbioru danych

**nazwa:** Edycja zbioru danych

**aktorzy:** Dostawca danych, System

**opis:**
    System umożliwia dostawcy danych edytowanie istniejącego zbioru danych. Proces edycji obejmuje możliwość zmiany opisu zbioru, kategorii, formatu pliku oraz innych metadanych. Zmiany wprowadzane przez dostawcę są walidowane przed zapisaniem w systemie. Walidacja danych jest realizowana jako osobny przypadek użycia **(include: Walidacja Danych)**.

**kroki:**
1. **Dostawca danych** wybiera opcję edytowania istniejącego zbioru danych.
2. **System** wyświetla formularz z obecnymi informacjami o zbiorze (np. nazwa, opis, kategorie, format pliku).
3. **Dostawca danych** wprowadza zmiany w formularzu i przesyła zaktualizowane dane.
4. **System** wykonuje przypadek użycia **Walidacja Danych**.
5. **System** zapisuje zaktualizowany zbiór danych w bazie i rejestruje zmiany w katalogu zbiorów.
6. **System** wyświetla komunikat potwierdzający pomyślną edycję zbioru danych.

**alt 1 Niepowodzenie walidacji danych:**
1. **System** wykrywa, że wprowadzone dane zawierają błędy (np. niepoprawny format, brak wymaganych informacji) w ramach przypadku użycia **Walidacja Danych**.
2. **System** wyświetla komunikat o błędach i prosi dostawcę danych o poprawienie i ponowne przesłanie zaktualizowanego zbioru danych.

##### UC0008 Walidacja danych

**nazwa:** Walidacja danych

**aktorzy:** System

**opis:**
    System sprawdza poprawność danych przesyłanych przez dostawcę danych. Walidacja obejmuje kontrolę formatu pliku, poprawności wymaganych pól oraz spójności danych. Celem jest zapewnienie, że przesłane dane są zgodne z wymaganiami systemu przed ich zapisaniem lub przetworzeniem.

**kroki:**
1. **System** otrzymuje dane od dostawcy danych.
2. **System** sprawdza, czy dane są w poprawnym formacie.
3. **System** weryfikuje, czy wszystkie wymagane pola są obecne i mają poprawny typ danych.
4. **System** sprawdza spójność danych (np. czy daty są w odpowiednim formacie, czy wartości mieszczą się w dozwolonym zakresie).
5. **System** zwraca wynik walidacji:
   - Jeśli dane są poprawne, proces przechodzi do zapisu lub dalszego przetwarzania.
   - Jeśli dane zawierają błędy, system zgłasza je dostawcy danych.

**alt 1 Niepoprawne dane:**
1. **System** wykrywa, że dane zawierają błędy (np. niepoprawny format, brak wymaganych pól, błędne wartości).
2. **System** wyświetla komunikat o błędach i prosi dostawcę danych o poprawienie błędów i ponowne przesłanie danych.

##### UC0009 Importowanie danych

**nazwa:** Importowanie danych

**aktorzy:** Dostawca danych, System

**opis:**
    System umożliwia dostawcy danych importowanie zbiorów danych do systemu. Importowanie danych obejmuje przesyłanie plików lub danych w odpowiednim formacie, które zostaną zapisane w systemie. Proces ten może obejmować walidację danych, kontrolę jakości oraz automatyczne mapowanie danych do struktury systemu.

**kroki:**
1. **Dostawca danych** wybiera opcję importu danych w systemie.
2. **System** wyświetla formularz lub interfejs do przesłania pliku z danymi.
3. **Dostawca danych** wybiera plik z danymi do importu i przesyła go do systemu.
4. **System** wykonuje przypadek użycia **Walidacja danych** w celu sprawdzenia poprawności przesłanych danych.
5. **System** mapuje dane z przesłanego pliku do odpowiednich struktur danych w systemie.
6. **System** zapisuje zaimportowane dane w bazie danych.
7. **System** wyświetla komunikat potwierdzający pomyślne zaimportowanie danych.

**alt 1 Niepowodzenie walidacji danych:**
1. **System** wykrywa, że dane w przesłanym pliku zawierają błędy (np. niepoprawny format, brak wymaganych pól).
2. **System** wyświetla komunikat o błędach i prosi dostawcę danych o poprawienie pliku oraz ponowne przesłanie danych.

**alt 2 Niepoprawny format pliku:**
1. **Dostawca danych** przesyła plik w nieobsługiwanym formacie (np. plik tekstowy, niespójny format CSV).
2. **System** wykrywa niepoprawny format pliku.
3. **System** wyświetla komunikat informujący o błędzie formatu pliku i prosi o przesłanie pliku w obsługiwanym formacie.

##### UC0010 Przypisywanie schematów do zbiorów danych

**nazwa:** Przypisywanie schematów do zbiorów danych

**aktorzy:** Dostawca danych, System

**opis:**
    System umożliwia dostawcy danych przypisanie schematu do zbioru danych. Schemat określa strukturę danych, w tym wymagane pola, formaty oraz inne zasady, które muszą być przestrzegane przy wprowadzaniu danych. Przypisanie schematu jest kluczowe, aby zapewnić spójność danych i umożliwić ich prawidłowe przetwarzanie w systemie.

**kroki:**
1. **Dostawca danych** wybiera opcję przypisania schematu do zbioru danych.
2. **System** wyświetla listę dostępnych schematów, które mogą być przypisane do zbioru danych.
3. **Dostawca danych** wybiera odpowiedni schemat z listy.
4. **System** przypisuje wybrany schemat do zbioru danych.
5. **System** zapisuje przypisanie schematu w bazie danych, aktualizując metadane zbioru.
6. **System** wyświetla komunikat potwierdzający przypisanie schematu do zbioru danych.

**alt 1 Brak dostępnych schematów:**
1. **Dostawca danych** wybiera opcję przypisania schematu, ale system nie ma dostępnych schematów w bazie.
2. **System** wyświetla komunikat informujący o braku dostępnych schematów do przypisania.

**alt 2 Błąd przy przypisywaniu schematu:**
1. **Dostawca danych** wybiera schemat i system próbuje go przypisać do zbioru danych.
2. **System** wykrywa błąd (np. konflikt schematu z istniejącymi danymi).
3. **System** wyświetla komunikat o błędzie i informuje dostawcę danych o konieczności wyboru innego schematu.

##### UC0011 Eksportowanie danych w różnych formatach

**nazwa:** Eksportowanie danych w różnych formatach

**aktorzy:** Klient/Użytkownik danych, System

**opis:**
    System umożliwia użytkownikowi eksportowanie danych w różnych formatach (np. CSV, JSON, XML, Excel). Proces eksportu pozwala na wygodne pobranie danych z systemu i ich dalsze przetwarzanie lub analiza w wybranym formacie. Użytkownik może wybrać format, który najlepiej odpowiada jego potrzebom.

**kroki:**
1. **Klient/Użytkownik danych** wybiera opcję eksportu danych.
2. **System** wyświetla dostępne formaty eksportu (np. CSV, JSON, XML, Excel).
3. **Klient/Użytkownik danych** wybiera preferowany format eksportu.
4. **System** generuje plik w wybranym formacie, zawierający dane do pobrania.
5. **System** umożliwia użytkownikowi pobranie wygenerowanego pliku.
6. **System** wyświetla komunikat potwierdzający pomyślne zakończenie eksportu.

**alt 1 Brak danych do eksportu:**
1. **Klient/Użytkownik danych** wybiera opcję eksportu danych.
2. **System** wykrywa, że brak jest dostępnych danych do eksportu (np. brak wyników dla wybranych filtrów).
3. **System** wyświetla komunikat informujący o braku danych do eksportu.

**alt 2 Błąd podczas generowania pliku:**
1. **Klient/Użytkownik danych** wybiera format eksportu.
2. **System** napotyka błąd podczas generowania pliku (np. problemy z formatowaniem, brak uprawnień).
3. **System** wyświetla komunikat o błędzie i informuje użytkownika o problemach z eksportem.

##### UC0012 Usuwanie zbioru danych

**nazwa:** Usuwanie zbiorów danych

**aktorzy:** Administrator systemu, System

**opis:**
    System umożliwia Administratorowi systemu usunięcie zbiorów danych z bazy. Usunięcie zbioru danych jest ostateczną akcją, która trwale usuwa dane z systemu. Proces usuwania może wymagać potwierdzenia, aby zapobiec przypadkowemu usunięciu danych.

**kroki:**
1. **Administrator systemu** wybiera opcję usunięcia zbioru danych.
2. **System** wyświetla listę dostępnych zbiorów danych do usunięcia.
3. **Administrator systemu** wybiera zbiór danych, który chce usunąć.
4. **System** wyświetla komunikat potwierdzający, informując, że operacja usunięcia jest nieodwracalna.
5. **Administrator systemu** potwierdza chęć usunięcia zbioru danych.
6. **System** usuwa wskazany zbiór danych z bazy.
7. **System** wyświetla komunikat potwierdzający pomyślne usunięcie zbioru danych.

**alt 1 Brak uprawnień:**
1. **Administrator systemu** próbuje usunąć zbiór danych.
2. **System** sprawdza uprawnienia administratora.
3. **System** wykrywa brak wymaganych uprawnień (np. brak uprawnień do usunięcia danych).
4. **System** wyświetla komunikat informujący o braku uprawnień do wykonania operacji.

**alt 2 Błąd podczas usuwania:**
1. **Administrator systemu** wybiera zbiór danych do usunięcia.
2. **System** napotyka błąd podczas próby usunięcia danych (np. problemy z bazą danych, brak dostępu do danych).
3. **System** wyświetla komunikat o błędzie i informuje administratora o problemach z usuwaniem zbioru danych.

##### UC0013 Archiwizacja zbiorów danych

**nazwa:** Archiwizacja zbiorów danych

**aktorzy:** Administrator systemu, System

**opis:**
    System umożliwia Administratorowi systemu archiwizowanie zbiorów danych, które nie są już aktywnie używane, ale muszą zostać zachowane w celu przechowywania lub przyszłego wykorzystania. Archiwizacja polega na przeniesieniu danych do specjalnej przestrzeni archiwalnej, gdzie będą mogły być bezpiecznie przechowywane. Po archiwizacji, dane są niedostępne do regularnego użytku, ale mogą być odzyskane, jeśli zajdzie taka potrzeba.

**kroki:**
1. **Administrator systemu** wybiera opcję archiwizacji zbioru danych.
2. **System** wyświetla listę dostępnych zbiorów danych, które mogą być archiwizowane.
3. **Administrator systemu** wybiera zbiór danych, który ma zostać zarchiwizowany.
4. **System** wyświetla komunikat potwierdzający, że zbiór danych zostanie przeniesiony do archiwum.
5. **Administrator systemu** potwierdza chęć archiwizacji zbioru danych.
6. **System** przenosi zbiór danych do przestrzeni archiwalnej, zmieniając jego status na "zarchiwizowany".
7. **System** wyświetla komunikat potwierdzający pomyślną archiwizację zbioru danych.

**alt 1 Brak uprawnień:**
1. **Administrator systemu** próbuje archiwizować zbiór danych.
2. **System** sprawdza uprawnienia administratora.
3. **System** wykrywa brak wymaganych uprawnień (np. brak uprawnień do archiwizacji).
4. **System** wyświetla komunikat informujący o braku uprawnień do wykonania operacji.

**alt 2 Błąd podczas archiwizacji:**
1. **Administrator systemu** wybiera zbiór danych do archiwizacji.
2. **System** napotyka błąd podczas próby archiwizacji (np. problemy z przestrzenią archiwalną lub dostępem do danych).
3. **System** wyświetla komunikat o błędzie i informuje administratora o problemach z archiwizowaniem zbioru danych.

##### UC0014 Przywracanie zbiorów danych

**nazwa:** Przywracanie zbiorów danych

**aktorzy:** Administrator systemu, System

**opis:**
    System umożliwia Administratorowi systemu przywracanie zbiorów danych, które zostały wcześniej zarchiwizowane. Przywracanie danych polega na przeniesieniu zarchiwizowanych zbiorów danych z przestrzeni archiwalnej do aktywnej bazy danych, aby mogły być ponownie używane w systemie. Proces przywracania danych może obejmować weryfikację integralności danych przed ich ponownym udostępnieniem.

**kroki:**
1. **Administrator systemu** wybiera opcję przywrócenia zbioru danych.
2. **System** wyświetla listę dostępnych zarchiwizowanych zbiorów danych, które mogą zostać przywrócone.
3. **Administrator systemu** wybiera zbiór danych, który ma zostać przywrócony.
4. **System** weryfikuje integralność danych przed przywróceniem (np. sprawdza, czy dane nie zostały uszkodzone w procesie archiwizacji).
5. **Administrator systemu** potwierdza chęć przywrócenia zbioru danych.
6. **System** przywraca zbiór danych z przestrzeni archiwalnej do aktywnej bazy danych.
7. **System** zmienia status zbioru danych na "aktywny" i umożliwia jego dalsze wykorzystanie.
8. **System** wyświetla komunikat potwierdzający pomyślne przywrócenie zbioru danych.

**alt 1 Brak uprawnień:**
1. **Administrator systemu** próbuje przywrócić zbiór danych.
2. **System** sprawdza uprawnienia administratora.
3. **System** wykrywa brak wymaganych uprawnień (np. brak uprawnień do przywracania danych).
4. **System** wyświetla komunikat informujący o braku uprawnień do wykonania operacji.

**alt 2 Błąd podczas przywracania:**
1. **Administrator systemu** wybiera zbiór danych do przywrócenia.
2. **System** napotyka błąd podczas próby przywrócenia danych (np. brak dostępu do archiwum, problemy z integracją danych).
3. **System** wyświetla komunikat o błędzie i informuje administratora o problemach z przywracaniem zbioru danych.




