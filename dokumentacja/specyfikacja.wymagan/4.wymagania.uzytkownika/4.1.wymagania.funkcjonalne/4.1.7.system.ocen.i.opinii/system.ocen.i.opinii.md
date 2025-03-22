#### Diagram

:[Diagram](diagram.puml)

#### Przypadki użycia

##### UC7001 Wystawienie oceny zbioru danych

**nazwa:** Wystawienie oceny zbioru danych

**aktorzy:** Klient/Użytkownik danych, System

**opis:**  
    System umożliwia użytkownikowi wystawienie oceny dla wybranego zbioru danych, co wpływa na jego ogólną ocenę oraz umożliwia innym użytkownikom zapoznanie się z opiniami.

**kroki:**
1. **Klient/Użytkownik danych** wybiera zbiór danych, który chce ocenić.
2. **System** wyświetla interfejs umożliwiający wystawienie oceny (np. skala od 1 do 5 gwiazdek) oraz dodanie komentarza.
3. **Klient/Użytkownik danych** wybiera wartość oceny oraz wpisuje opcjonalny komentarz.
4. **Klient/Użytkownik danych** zatwierdza wystawienie oceny.
5. **System** zapisuje ocenę i aktualizuje średnią ocen zbioru.
6. **System** wyświetla komunikat potwierdzający pomyślne wystawienie oceny.

**alt 1 – Nieprawidłowa wartość oceny:**  
1. **System** wykrywa nieprawidłowy format lub zakres oceny.
2. **System** wyświetla komunikat o konieczności poprawienia wprowadzonych danych.

---

##### UC7002 Aktualizacja oceny zbioru danych

**nazwa:** Aktualizacja oceny zbioru danych

**aktorzy:** Klient/Użytkownik danych, System

**opis:**  
    System umożliwia użytkownikowi aktualizację wcześniej wystawionej oceny, w tym zmianę wartości oraz komentarza.

**kroki:**
1. **Klient/Użytkownik danych** loguje się i wybiera zbiór danych, dla którego chce zaktualizować ocenę.
2. **System** wyświetla dotychczasową ocenę i komentarz.
3. **Klient/Użytkownik danych** modyfikuje wartość oceny oraz/lub komentarz.
4. **Klient/Użytkownik danych** zatwierdza zmiany.
5. **System** zapisuje zaktualizowaną ocenę oraz przelicza średnią ocen zbioru.
6. **System** wyświetla komunikat potwierdzający pomyślną aktualizację oceny.

**alt 1 – Błąd podczas aktualizacji:**  
1. **System** wykrywa błąd przy zapisie zmienionej oceny.
2. **System** wyświetla komunikat o błędzie i prosi o ponowne wprowadzenie zmian.

---

##### UC7003 Wyświetlenie historii ocen

**nazwa:** Wyświetlenie historii ocen

**aktorzy:** Klient/Użytkownik danych, System

**opis:**  
    System umożliwia użytkownikowi przeglądanie historii ocen wystawionych dla danego zbioru danych, wraz z datami i komentarzami.

**kroki:**
1. **Klient/Użytkownik danych** wybiera zbiór danych, dla którego chce zobaczyć historię ocen.
2. **System** pobiera historię ocen z bazy danych.
3. **System** generuje listę zawierającą szczegóły każdej oceny (data, wartość, komentarz).
4. **System** wyświetla historię ocen użytkownikowi.

**alt 1 – Brak historii ocen:**  
1. **System** wyświetla komunikat informujący, że dla wybranego zbioru nie ma zarejestrowanych ocen.
