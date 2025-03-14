## Cechy funkcjonalne systemu

System Zarządzania Otwartymi Danymi Publicznymi powinien realizować następujące funkcjonalności, pogrupowane według stopnia ważności.

### Priorytet wysoki

1. **Zarządzanie metadanymi udostępnionych zbiorów danych**
   * System musi umożliwiać przechowywanie i zarządzanie metadanymi opisującymi zbiory danych.
   * Metadane powinny zawierać informacje o źródle danych, dacie utworzenia, aktualizacji, formacie, itp.

2. **Zarządzanie dystrybucjami zbiorów danych i ich powiązanie ze źródłami danych**
   * System powinien umożliwiać zarządzanie różnymi dystrybucjami tych samych zbiorów danych.
   * Musi istnieć możliwość śledzenia pochodzenia danych i powiązania ich ze źródłami.

3. **Możliwość wygodnego wprowadzania, przeglądania, filtrowania i wyszukiwania zbiorów danych i ich dystrybucji**
   * System powinien zapewniać intuicyjny interfejs do wprowadzania nowych danych.
   * Użytkownicy muszą mieć możliwość efektywnego przeszukiwania i filtrowania zbiorów danych.

4. **Zarządzanie schematami danych i przypisywanie schematów danych do zbiorów danych**
   * System musi umożliwiać definiowanie schematów danych.
   * Użytkownik powinien móc przypisywać schematy do odpowiednich zbiorów danych.

5. **Weryfikacja zgodności dystrybucji zbiorów danych ze schematami**
   * System powinien automatycznie weryfikować, czy dane są zgodne z przypisanymi schematami.
   * W przypadku wykrycia niezgodności, system musi informować o problemach.

6. **Import i eksport danych w różnych formatach z zachowaniem zgodności ze schematami**
   * System musi obsługiwać import danych z różnych źródeł i w różnych formatach.
   * Eksport danych powinien być możliwy w wielu formatach, z zachowaniem zgodności ze schematami.

7. **Integracja z systemem CKAN**
   * System powinien integrować się z platformą CKAN do zarządzania danymi.
   * Integracja powinna umożliwiać wymianę danych między systemami.

8. **Filtrowanie i wyszukiwanie danych**
   * Użytkownicy powinni móc filtrować dane według różnych kryteriów.
   * System musi zapewniać zaawansowane mechanizmy wyszukiwania.

9. **Autentykacja danych**
   * System musi weryfikować autentyczność danych.
   * Powinien istnieć mechanizm weryfikacji źródła danych.

10. **Autoryzacja użytkowników**
    * System musi posiadać mechanizm zarządzania uprawnieniami użytkowników.
    * Różni użytkownicy powinni mieć różne poziomy dostępu.

11. **Przyznawanie dostępu**
    * Administrator powinien móc przyznawać i odbierać dostęp do systemu.
    * System musi umożliwiać definiowanie ról i uprawnień.

12. **Sprawdzenie poziomu dostępu użytkownika**
    * System musi weryfikować uprawnienia użytkownika przed wykonaniem operacji.
    * Poziomy dostępu powinny być sprawdzane w czasie rzeczywistym.

13. **Dodawanie danych przez API**
    * System musi udostępniać API do automatycznego dodawania danych.
    * API powinno być dobrze udokumentowane i zabezpieczone.

14. **Prezentowanie wszystkich zbiorów danych**
    * System musi prezentować listę wszystkich dostępnych zbiorów danych.
    * Prezentacja powinna być przejrzysta i umożliwiać sortowanie.

15. **Ulepszanie jakości danych**
    * System powinien posiadać mechanizmy do poprawy jakości przechowywanych danych.
    * Należy implementować procesy weryfikacji i czyszczenia danych.

16. **Utrzymanie aktualności danych**
    * System musi zapewniać mechanizmy regularnego aktualizowania danych.
    * Użytkownicy powinni być informowani o statusie aktualności danych.

17. **Wykrywanie anomalii**
    * System powinien automatycznie wykrywać anomalie i niespójności w danych.
    * O wykrytych anomaliach system powinien informować odpowiedzialnych użytkowników.

18. **Zapewnienie bezpieczeństwa danych**
    * System musi implementować mechanizmy zabezpieczające dane przed nieautoryzowanym dostępem.
    * Należy stosować odpowiednie mechanizmy kryptograficzne i kontroli dostępu.

19. **Wykrywanie błędów w zbiorach**
    * System powinien automatycznie wykrywać błędy w zbiorach danych.
    * Wykryte błędy powinny być raportowane i oznaczane do korekty.

20. **Szyfrowanie danych wrażliwych**
    * Dane wrażliwe muszą być przechowywane w formie zaszyfrowanej.
    * System powinien automatycznie rozpoznawać i szyfrować wrażliwe informacje.

21. **Szyfrowanie przesyłu**
    * Komunikacja z systemem musi być szyfrowana.
    * Należy stosować aktualne protokoły kryptograficzne do zabezpieczenia transmisji.

22. **Automatyczna cykliczna walidacja zbiorów**
    * System powinien cyklicznie przeprowadzać walidację zbiorów danych.
    * Wyniki walidacji powinny być raportowane odpowiednim użytkownikom.

### Priorytet średni

1. **System ocen oraz uwag od użytkowników**
   * Użytkownicy powinni móc oceniać zbiory danych i pozostawiać komentarze.
   * System powinien agregować i wyświetlać oceny.

2. **Prezentacja wyników wyszukiwania w różnych formatach**
   * System powinien prezentować wyniki wyszukiwania w różnych formatach (tabele, wykresy).
   * Użytkownik powinien móc wybierać sposób prezentacji.

3. **Wyodrębnianie kluczowych wskaźników**
   * System powinien automatycznie analizować dane i wyodrębniać kluczowe wskaźniki.
   * Wskaźniki powinny być prezentowane w czytelny sposób.

4. **Zgłaszanie błędów danych**
   * Użytkownicy powinni móc zgłaszać błędy w danych.
   * System powinien zarządzać zgłoszeniami i umożliwiać ich weryfikację.

5. **Generowanie raportów**
   * System musi umożliwiać generowanie raportów na podstawie danych.
   * Raporty powinny być dostępne w różnych formatach.

6. **Przedstawienie historii zmian w przystępny sposób**
   * System powinien śledzić historię zmian w danych.
   * Historia zmian powinna być prezentowana w sposób czytelny dla użytkownika.

7. **Powiadomienia o aktualizacjach**
   * System powinien informować użytkowników o aktualizacjach zbiorów danych.
   * Użytkownicy powinni móc subskrybować powiadomienia dla określonych zbiorów.

8. **Integracja narzędzi do wizualizacji danych**
   * System powinien integrować narzędzia umożliwiające wizualizację danych.
   * Wizualizacje powinny być interaktywne i konfigurowalne.

9. **Aktualizowanie wybranych zbiorów co sekundę**
   * System powinien umożliwiać częste aktualizacje wybranych zbiorów danych.
   * Mechanizm aktualizacji powinien być wydajny i nie obciążać systemu.

10. **Udostępnianie danych wyżej w hierarchii**
    * System powinien umożliwiać udostępnianie wybranych zbiorów danych na wyższe poziomy hierarchii.
    * Proces udostępniania powinien być kontrolowany i zabezpieczony.

11. **Archiwizacja danych**
    * System powinien automatycznie archiwizować starsze dane.
    * Dane archiwalne powinny być dostępne na żądanie.

12. **Wersjonowanie danych**
    * System musi umożliwiać przechowywanie różnych wersji tych samych zbiorów danych.
    * Użytkownicy powinni mieć możliwość porównania różnych wersji danych.

13. **Przechowywanie logów systemu w celu audytu**
    * System powinien przechowywać logi wszystkich operacji.
    * Logi powinny być dostępne na potrzeby audytu i analizy bezpieczeństwa.

14. **Zbieranie i analizowanie ocen użytkowników**
    * System powinien zbierać opinie użytkowników o danych i funkcjonalnościach.
    * Zebrane opinie powinny być analizowane w celu poprawy jakości systemu.

15. **Automatyzacja aktualizacji**
    * System powinien umożliwiać automatyczne aktualizacje danych z zewnętrznych źródeł.
    * Proces aktualizacji powinien być monitorowany i raportowany.

16. **Analiza wykorzystania danych**
    * System powinien analizować, które zbiory danych są najczęściej używane.
    * Analiza powinna dostarczać informacji o wzorcach korzystania z danych.

17. **Wykrywanie zagrożeń bezpieczeństwa**
    * System powinien monitorować próby nieautoryzowanego dostępu.
    * O potencjalnych zagrożeniach powinni być informowani administratorzy.

18. **Monitorowanie wydajności**
    * System powinien monitorować swoją wydajność i obciążenie.
    * W przypadku problemów wydajnościowych powinny być generowane alerty.

### Priorytet niski

1. **Zapewnienie tłumaczenia na inne języki**
   * System powinien wspierać wielojęzyczność.
   * Interfejs i dane powinny być dostępne w różnych językach.

2. **Statystyki wyszukiwań**
   * System powinien zbierać statystyki dotyczące wyszukiwań.
   * Statystyki powinny być dostępne dla administratorów.

3. **Ocena UI**
   * Użytkownicy powinni móc oceniać interfejs użytkownika.
   * System powinien zbierać opinie na temat użyteczności.

4. **Śledzenie aktywności użytkownika w ocenianiu**
   * System powinien śledzić aktywność użytkowników związaną z ocenianiem zbiorów.
   * Informacje te powinny być wykorzystywane do poprawy jakości danych.

5. **Ocenianie danych pod kątem przydatności**
   * Użytkownicy powinni móc oceniać przydatność danych.
   * System powinien uwzględniać te oceny w algorytmach wyszukiwania.

6. **Zarabianie na reklamach**
   * System może posiadać mechanizmy monetyzacji poprzez wyświetlanie reklam.
   * Reklamy powinny być nieinwazyjne i związane z kontekstem.

7. **Wspieranie badań naukowych poprzez dostarczanie zbiorów**
   * System powinien oferować specjalne funkcje dla użytkowników akademickich.
   * Dane powinny być przygotowane w formacie odpowiednim dla celów badawczych.

8. **Cachowanie odpowiedzi**
   * System powinien implementować mechanizmy cachowania dla częstych zapytań.
   * Cachowanie powinno optymalizować wydajność i zmniejszać obciążenie bazy danych.
