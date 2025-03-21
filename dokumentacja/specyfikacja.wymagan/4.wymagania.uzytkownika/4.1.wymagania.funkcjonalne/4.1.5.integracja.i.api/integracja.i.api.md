#### Diagram

:[Diagram](diagram.puml)

#### Przypadki użycia


#### UC0032 Dodanie danych przez API
**nazwa:** Dodanie danych przez API

**aktorzy:** System zewnętrzny, System  
**opis:**  
System umożliwia zewnętrznym systemom dodawanie danych za pomocą API. Proces obejmuje przesłanie danych w odpowiednim formacie, ich walidację oraz zapisanie w systemie.  

**kroki:**  
1. **System zewnętrzny** wysyła żądanie dodania danych do API.  
2. **System** odbiera żądanie i weryfikuje poprawność przesłanych danych.  
3. **System** zapisuje dane w bazie danych.  
4. **System** zwraca odpowiedź o pomyślnym dodaniu danych.  

**alt 1 Niepoprawne dane:**  
1. **System** wykrywa, że przesłane dane są niepoprawne.
2. **System** zwraca odpowiedź z informacją o błędzie i szczegółami problemu.  


#### UC0033 Uaktualnienie danych przez API
**nazwa:** Uaktualnienie danych przez API

**aktorzy:** System zewnętrzny, System  
**opis:**  
System umożliwia zewnętrznym systemom aktualizację istniejących danych za pomocą API. Proces obejmuje przesłanie danych do aktualizacji, ich walidację oraz zapisanie zmian w systemie.  

**kroki:**  
1. **System zewnętrzny** wysyła żądanie aktualizacji danych do API.  
2. **System** odbiera żądanie i weryfikuje poprawność przesłanych danych.  
3. **System** aktualizuje dane w bazie danych.  
4. **System** zwraca odpowiedź o pomyślnym uaktualnieniu danych.  

**alt 1 Niepoprawne dane:**  
1. **System** wykrywa, że przesłane dane są niepoprawne.  
2. **System** zwraca odpowiedź z informacją o błędzie i szczegółami problemu.  


#### UC0034 Usunięcie danych przez API
**nazwa:** Usunięcie danych przez API

**aktorzy:** System zewnętrzny, System  
**opis:**  
System umożliwia zewnętrznym systemom usuwanie danych za pomocą API. Proces obejmuje przesłanie identyfikatora danych do usunięcia, weryfikację żądania oraz usunięcie danych z systemu.  

**kroki:**  
1. **System zewnętrzny** wysyła żądanie usunięcia danych do API.  
2. **System** odbiera żądanie i weryfikuje poprawność przesłanych danych.
3. **System** usuwa dane z bazy danych.  
4. **System** zwraca odpowiedź o pomyślnym usunięciu danych.  

**alt 1 Dane nie istnieją:**  
1. **System** wykrywa, że dane do usunięcia nie istnieją w bazie danych.  
2. **System** zwraca odpowiedź z informacją o błędzie.  


#### UC0035 Integracja z CKAN
**nazwa:** Integracja z CKAN

**aktorzy:** Administrator systemu, System, CKAN  
**opis:**  
System umożliwia integrację z platformą CKAN w celu synchronizacji danych. Proces obejmuje konfigurację integracji, przesyłanie danych do CKAN oraz odbieranie danych z CKAN.  

**kroki:**
2. **Administrator systemu** przechodzi do sekcji konfiguracji integracji z CKAN.  
3. **Administrator systemu** wprowadza dane konfiguracyjne.
4. **Administrator systemu** zatwierdza konfigurację.  
5. **System** nawiązuje połączenie z platformą CKAN i weryfikuje poprawność konfiguracji.  
6. **System** synchronizuje dane z platformą CKAN.
7. **System** wyświetla komunikat o pomyślnym zakończeniu integracji.  

**alt 1 Błąd konfiguracji:**  
1. **System** wykrywa, że dane konfiguracyjne są niepoprawne.
2. **System** wyświetla komunikat o błędzie i prosi administratora o poprawienie konfiguracji.  

**alt 2 Błąd synchronizacji:**  
1. **System** napotyka błąd podczas synchronizacji z CKAN.  
2. **System** wyświetla komunikat o błędzie..  