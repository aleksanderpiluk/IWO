#### Diagram

:[Diagram](diagram.puml)

#### Przypadki użycia
##### UC6001 Generowanie raportów dot. bezpieczeństwa

**nazwa:** Generowanie raportów dotyczących bezpieczeństwa

**aktorzy:** Klient/Użytkownik danych, System

**opis:**  
    System umożliwia generowanie raportów dotyczących bezpieczeństwa danych, zawierających informacje o incydentach, nieautoryzowanym dostępie i innych zagrożeniach.

**kroki:**
1. **Klient/Użytkownik danych** wybiera opcję "Generuj raport bezpieczeństwa".
2. **System** wyświetla dostępne kryteria (np. okres, typ incydentu).
3. **Klient/Użytkownik danych** wybiera kryteria i zatwierdza wybór.
4. **System** generuje raport na podstawie wybranych kryteriów.
5. **System** zapisuje raport i udostępnia go użytkownikowi.

**alt 1 – Błąd generowania raportu:**  
1. **System** wykrywa problem podczas generowania raportu.  
2. **System** wyświetla komunikat o błędzie i sugeruje ponowną próbę.

---

##### UC6002 Analiza raportów dot. bezpieczeństwa

**nazwa:** Analiza raportów dotyczących bezpieczeństwa

**aktorzy:** Klient/Użytkownik danych, System

**opis:**  
    System umożliwia analizę wygenerowanych raportów dotyczących bezpieczeństwa, co pozwala na identyfikację trendów i potencjalnych zagrożeń.

**kroki:**
1. **Klient/Użytkownik danych** wybiera opcję "Analizuj raport bezpieczeństwa".
2. **System** wyświetla listę dostępnych raportów bezpieczeństwa.
3. **Klient/Użytkownik danych** wybiera raport do analizy.
4. **System** prezentuje szczegółowe dane raportu (np. wykresy, tabele, wskaźniki).
5. **Klient/Użytkownik danych** dokonuje analizy raportu.

**alt 1 – Brak raportów:**  
1. **System** wyświetla komunikat o braku dostępnych raportów bezpieczeństwa.

---

##### UC6003 Generowanie raportów dot. wydajności

**nazwa:** Generowanie raportów dotyczących wydajności

**aktorzy:** Klient/Użytkownik danych, System

**opis:**  
    System umożliwia tworzenie raportów dotyczących wydajności systemu, prezentujących statystyki takie jak obciążenie serwera, czas reakcji i inne kluczowe metryki.

**kroki:**
1. **Klient/Użytkownik danych** wybiera opcję "Generuj raport wydajności".
2. **System** prezentuje dostępne kryteria raportowania (np. okres, wybrane metryki).
3. **Klient/Użytkownik danych** wybiera kryteria i zatwierdza wybór.
4. **System** generuje raport na podstawie podanych kryteriów.
5. **System** zapisuje i udostępnia raport użytkownikowi.

**alt 1 – Błąd generowania raportu:**  
1. **System** wyświetla komunikat o błędzie i sugeruje ponowną próbę generacji.

---

##### UC6004 Analiza raportów dot. wydajności

**nazwa:** Analiza raportów dotyczących wydajności

**aktorzy:** Klient/Użytkownik danych, System

**opis:**  
    System umożliwia analizę wygenerowanych raportów wydajności, co pozwala na ocenę działania systemu oraz identyfikację potencjalnych usprawnień.

**kroki:**
1. **Klient/Użytkownik danych** wybiera opcję "Analizuj raport wydajności".
2. **System** prezentuje listę dostępnych raportów wydajności.
3. **Klient/Użytkownik danych** wybiera raport do analizy.
4. **System** wyświetla szczegóły raportu (wykresy, tabele, statystyki).
5. **Klient/Użytkownik danych** dokonuje analizy raportu.

**alt 1 – Raport nie zawiera danych:**  
1. **System** wyświetla komunikat informujący, że raport nie zawiera wystarczających danych do analizy.

---

##### UC6005 Raportowanie o ruchu

**nazwa:** Raportowanie o ruchu

**aktorzy:** Klient/Użytkownik danych, System

**opis:**  
    System generuje raporty dotyczące ruchu w systemie, prezentując statystyki takie jak liczba użytkowników, liczba operacji oraz inne metryki aktywności.

**kroki:**
1. **Klient/Użytkownik danych** wybiera opcję "Raportuj ruch".
2. **System** zbiera dane o ruchu w określonym okresie.
3. **System** generuje raport zawierający kluczowe metryki.
4. **System** wyświetla raport użytkownikowi.

**alt 1 – Brak danych o ruchu:**  
1. **System** wyświetla komunikat o braku dostępnych danych do raportowania.

---

##### UC6006 Lista wygenerowanych raportów

**nazwa:** Lista wygenerowanych raportów

**aktorzy:** Klient/Użytkownik danych, System

**opis:**  
    System umożliwia przeglądanie historii wygenerowanych raportów, wraz z metadanymi (data, typ raportu) oraz opcją pobrania lub dalszej analizy.

**kroki:**
1. **Klient/Użytkownik danych** wybiera opcję "Lista raportów".
2. **System** pobiera listę wszystkich wygenerowanych raportów z bazy.
3. **System** wyświetla listę raportów z informacjami o dacie, typie oraz innymi metadanymi.
4. **Klient/Użytkownik danych** wybiera raport do pobrania lub analizy.

**alt 1 – Brak wygenerowanych raportów:**  
1. **System** wyświetla komunikat informujący o braku wygenerowanych raportów.
