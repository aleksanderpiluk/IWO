#### Diagram

:[Diagram](diagram.puml)

#### Przypadki użycia

##### UC0045 Tworzenie kopii zapasowych

**nazwa:** Tworzenie kopii zapasowych

**aktorzy:** Administrator systemu, System

**opis:**
    System umożliwia Administratorowi systemu tworzenie kopii zapasowych danych przechowywanych w systemie. Kopie zapasowe są tworzone w celu zabezpieczenia danych przed ich utratą w wyniku awarii systemu, błędów użytkownika lub innych nieprzewidzianych okoliczności. Proces tworzenia kopii zapasowej obejmuje zapisywanie danych w bezpiecznej lokalizacji, gdzie będą mogły zostać przywrócone w przypadku potrzeby.

**kroki:**
1. **Administrator systemu** wybiera opcję tworzenia kopii zapasowej.
2. **System** inicjuje proces tworzenia kopii zapasowej danych.
3. **System** wybiera dane, które mają zostać uwzględnione w kopii zapasowej (np. wszystkie dane, wybrane zbiory danych, konfiguracje systemowe).
4. **System** tworzy kopię zapasową i zapisuje ją w wybranej lokalizacji (np. chmura, zewnętrzny serwer, nośnik fizyczny).
5. **System** wyświetla komunikat potwierdzający pomyślne zakończenie tworzenia kopii zapasowej.

**alt 1 Brak dostępnej przestrzeni na kopię zapasową:**
1. **Administrator systemu** wybiera opcję tworzenia kopii zapasowej.
2. **System** sprawdza dostępność przestrzeni do zapisania kopii zapasowej.
3. **System** wykrywa brak wystarczającej przestrzeni do zapisania kopii zapasowej.
4. **System** wyświetla komunikat o błędzie i informuje administratora o braku miejsca na kopię zapasową.

**alt 2 Błąd podczas tworzenia kopii zapasowej:**
1. **Administrator systemu** wybiera opcję tworzenia kopii zapasowej.
2. **System** napotyka błąd podczas próby zapisania kopii zapasowej (np. problemy z dostępem do nośnika danych, błąd w procesie zapisu).
3. **System** wyświetla komunikat o błędzie i informuje administratora o problemach z tworzeniem kopii zapasowej.


