## Cechy jakościowe systemu

System Zarządzania Otwartymi Danymi Publicznymi powinien spełniać następujące wymagania jakościowe, pogrupowane według priorytetu.

### Priorytet wysoki

1. **Efektywne zarządzanie zbiorami danych**
   * System powinien umożliwiać efektywne i ergonomiczne zarządzanie zbiorami danych.
   * Interfejs zarządzania powinien być intuicyjny i minimalizować liczbę kroków potrzebnych do wykonania operacji.

2. **Zapewnienie stałego dostępu do danych**
   * System musi zapewniać nieprzerwany dostęp do danych z minimalną liczbą niedostępności.
   * Architektura powinna być redundantna, aby zapobiegać przestojom.

3. **Time to recovery**
   * W przypadku awarii, czas przywracania funkcjonalności systemu nie powinien przekraczać 2 godzin.
   * Proces odzyskiwania powinien być zautomatyzowany i regularnie testowany.

4. **Ochrona przed atakami**
   * System powinien posiadać zabezpieczenia przed typowymi atakami sieciowymi (DDoS, SQL Injection, XSS).
   * Regularne testy penetracyjne i audyty bezpieczeństwa powinny być przeprowadzane.

5. **Ciągłość działania**
   * System powinien działać bez przerw, z minimalnymi planowanymi przerwami technicznymi.
   * Aktualizacje systemu powinny odbywać się bez całkowitego wyłączania usługi.

6. **Przejrzystość interfejsu**
   * Interfejs użytkownika powinien być intuicyjny i łatwy w obsłudze dla użytkowników o różnym poziomie zaawansowania.
   * Elementy interfejsu powinny być logicznie pogrupowane i opisane.

7. **Sprawne dodawanie nowych źródeł danych**
   * Proces dodawania nowych źródeł danych powinien być prosty i szybki w implementacji.
   * Dodawanie nowego źródła powinno wymagać minimalnej konfiguracji.

8. **Zmniejszenie kosztów działania**
   * System powinien optymalizować wykorzystanie zasobów, aby minimalizować koszty operacyjne.
   * Automatyzacja rutynowych operacji powinna redukować koszty utrzymania.

### Priorytet średni

1. **SLA (poziom dostępności)**
   * System powinien zapewniać poziom dostępności (SLA) na poziomie 99.99999% (tzw. "seven nines").
   * Monitoring dostępności powinien umożliwiać szybką reakcję na problemy.

2. **Zminimalizowanie czasu wyszukiwania**
   * Czas potrzebny na wyszukanie danych powinien być jak najkrótszy.
   * Maksymalny czas przeszukiwania zbiorów danych nie powinien przekraczać 20 sekund, nawet przy złożonych zapytaniach.

3. **Skalowalność systemu**
   * Architektura powinna umożliwiać skalowanie poziome i pionowe w zależności od rosnącego obciążenia.
   * System powinien automatycznie dostosowywać wykorzystanie zasobów do bieżącego zapotrzebowania.

4. **Minimalizacja opóźnień**
   * System powinien być zoptymalizowany pod kątem minimalizacji opóźnień w dostępie do danych.
   * Opóźnienia w przesyłaniu i przetwarzaniu danych powinny być monitorowane i optymalizowane.

5. **Wsparcie dla różnych formatów**
   * System powinien obsługiwać szeroki zakres formatów danych wejściowych i wyjściowych.
   * Konwersja między formatami powinna odbywać się bez utraty informacji.

6. **Adaptacyjność UI**
   * Interfejs powinien być w pełni responsywny i dostosowywać się do różnych rozmiarów ekranów (desktop, tablet, telefon).
   * Układ elementów interfejsu powinien automatycznie reagować na zmianę rozdzielczości ekranu.

7. **Efektywność wprowadzania danych**
   * Proces wprowadzania nowych danych nie powinien zajmować więcej niż 2 minuty.
   * Interfejs wprowadzania danych powinien oferować podpowiedzi i automatyczne uzupełnianie.

8. **Archiwizacja danych**
   * Dane historyczne powinny być archiwizowane w sposób efektywny, nie obciążający głównej bazy danych.
   * System archiwizacji powinien umożliwiać szybkie przywracanie archiwalnych danych w razie potrzeby.

9. **Szybkość powiadomień**
   * Czas od wysłania do otrzymania powiadomienia nie powinien przekraczać 5 minut.
   * System powinien optymalizować dostarczanie powiadomień w zależności od ich priorytetu.

10. **Szybkość aktualizacji danych**
    * Wybrane, krytyczne zbiory danych powinny być aktualizowane w czasie rzeczywistym, z opóźnieniem nieprzekraczającym jednej sekundy.
    * Mechanizm aktualizacji powinien być wydajny i nie obciążać nadmiernie systemu.

### Priorytet niski

1. **Śledzenie aktywności użytkowników**
   * System powinien śledzić aktywność użytkowników związaną z ocenianiem zbiorów danych.
   * Dane o aktywności powinny być analizowane w celu poprawy jakości systemu.

2. **Szybkość generowania raportów**
   * Generowanie standardowych raportów powinno zajmować mniej niż jedną minutę.
   * System powinien optymalizować proces generowania raportów poprzez wstępne przetwarzanie danych.

3. **Dostępność dla osób z niepełnosprawnościami**
   * Interfejs powinien spełniać standardy dostępności WCAG 2.1 AA.
   * System powinien być kompatybilny z technologiami wspomagającymi używanymi przez osoby z niepełnosprawnościami.
