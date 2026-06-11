# Magazyn PWA

Aplikacja typu **Progressive Web Application (PWA)** wspomagająca zarządzanie lokalizacjami magazynowymi.

Projekt umożliwia szybkie sprawdzanie lokalizacji produktu, zmianę lokalizacji, rejestrowanie historii zmian oraz zarządzanie użytkownikami przy wykorzystaniu **Google Apps Script** i **Arkuszy Google** jako backendu.

---

# Funkcjonalności

## Zarządzanie użytkownikami

* wybór użytkownika z listy pobieranej z backendu,
* zapamiętywanie aktywnego użytkownika,
* rejestrowanie użytkownika wykonującego operacje magazynowe.

## Sprawdzanie lokalizacji

* wyszukiwanie produktu po kodzie,
* wyświetlanie aktualnej lokalizacji,
* szybki dostęp do historii zmian lokalizacji.

## Zmiana lokalizacji

* odczyt bieżącej lokalizacji produktu,
* przypisanie nowej lokalizacji,
* automatyczny zapis historii zmian.

## Historia zmian

Dla każdej zmiany zapisywane są informacje:

* data i godzina operacji,
* użytkownik wykonujący zmianę,
* poprzednia lokalizacja,
* nowa lokalizacja,
* identyfikator produktu.

## Konfiguracja urządzenia

* Device ID,
* Token 1,
* Token 2,
* lokalny zapis ustawień urządzenia.

## PWA (Progressive Web Application)

* możliwość instalacji na telefonie,
* możliwość instalacji na komputerze,
* działanie bez konieczności publikacji w sklepie Google Play,
* obsługa pliku manifest oraz Service Worker.

---

# Wykorzystane technologie

## Frontend

* HTML5
* CSS3
* JavaScript (Vanilla JS)

## Backend

* Google Apps Script

## Baza danych

* Google Sheets

## Hosting

* GitHub Pages

---

# Struktura projektu

```text
.
├── index.html
├── main.js
├── manifest.json
├── service-worker.js
├── JSONP_Code.gs
├── Magazyn.xlsx
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
└── README.md
```

---

# Struktura arkusza

Projekt wykorzystuje następujące zakładki:

## Magazyn

Przechowuje dane produktów oraz ich aktualne lokalizacje magazynowe.

## HistoriaZmian

Przechowuje historię wszystkich zmian lokalizacji.

## Uzytkownicy

Lista użytkowników dostępnych w aplikacji.

## AktywniUzytkownicy

Lista aktualnie aktywnych użytkowników.

## Autoryzacje

Lista autoryzowanych urządzeń wraz z przypisanymi tokenami.

---

# Instalacja

## 1. Przygotowanie arkusza Google

1. Prześlij plik `Magazyn.xlsx` na Dysk Google.
2. Otwórz plik.
3. Wybierz:

```text
Plik → Zapisz jako plik Arkuszy Google
```

4. Powstanie nowy arkusz w formacie Google Sheets.
5. Otwórz nowo utworzony arkusz.

---

## 2. Konfiguracja Google Apps Script

1. Otwórz utworzony wcześniej arkusz Google.
2. Wybierz:

```text
Rozszerzenia → Apps Script
```

3. Usuń domyślną zawartość projektu.
4. Wklej kod z pliku:

```text
JSONP_Code.gs
```

5. Zapisz projekt.

---

## 3. Publikacja aplikacji Apps Script

1. Wybierz:

```text
Wdrożenia → Nowe wdrożenie
```

2. Typ wdrożenia:

```text
Aplikacja internetowa
```

3. Ustaw:

```text
Uruchamiaj jako:
Ja

Kto ma dostęp:
Każdy
```

4. Zatwierdź wdrożenie.
5. Skopiuj wygenerowany adres URL aplikacji.

---

## 4. Nadanie uprawnień

Po utworzeniu wdrożenia należy jednorazowo uruchomić aplikację Apps Script.

1. Otwórz wygenerowany adres URL w przeglądarce.
2. Google poprosi o przyznanie wymaganych uprawnień.
3. Zaakceptuj wszystkie wymagane zgody.

Po wykonaniu tego kroku backend będzie gotowy do pracy.

---

## 5. Konfiguracja aplikacji

1. Uruchom aplikację.
2. Wejdź do sekcji:

```text
Ustawienia
```

3. Wprowadź:

* Device ID,
* Token 1,
* Token 2.

4. Zapisz konfigurację.

---

# Uruchomienie

## Lokalnie

Otwórz plik:

```text
index.html
```

lub uruchom projekt przy pomocy dowolnego lokalnego serwera HTTP.

---

## GitHub Pages

Aplikacja może zostać opublikowana poprzez GitHub Pages.

1. Wejdź do ustawień repozytorium.
2. Otwórz zakładkę:

```text
Settings → Pages
```

3. Wybierz:

```text
Deploy from a branch
```

4. Wskaż gałąź:

```text
main
```

5. Zapisz ustawienia.

Po kilku minutach aplikacja będzie dostępna pod adresem:

```text
https://twoj-login.github.io/nazwa-repozytorium/
```

---

# Wersja demonstracyjna

Repozytorium zawiera przykładowy plik `Magazyn.xlsx`, który umożliwia szybkie uruchomienie projektu bez konieczności samodzielnego tworzenia struktury arkusza.

---

# Informacje dotyczące bezpieczeństwa

Hasło w sekcji ustawień służy wyłącznie do ochrony lokalnej konfiguracji urządzenia.

Nie zapewnia ono ochrony danych magazynowych ani nie pełni funkcji autoryzacji użytkowników systemu. Błędna konfiguracja może jedynie uniemożliwić działanie aplikacji na danym urządzeniu.

---

# Autor

Pandaren256 (Mateusz Babiński)

Projekt wykonany w ramach zajęć akademickich oraz rozwijany jako praktyczne narzędzie wspomagające pracę magazynową.
