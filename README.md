# Magazyn PWA

Aplikacja typu Progressive Web Application (PWA) wspomagająca zarządzanie lokalizacjami magazynowymi. System umożliwia szybkie sprawdzanie aktualnej lokalizacji produktu, zmianę lokalizacji oraz rejestrowanie historii operacji wykonywanych przez użytkowników.

Projekt wykorzystuje Google Apps Script jako warstwę backendową oraz Arkusze Google jako bazę danych.

## Funkcjonalności

### Zarządzanie użytkownikami

* wybór użytkownika z listy pobieranej z backendu,
* zapamiętywanie aktywnego użytkownika,
* rejestrowanie użytkownika wykonującego operacje magazynowe.

### Sprawdzanie lokalizacji

* wyszukiwanie produktu po kodzie,
* wyświetlanie aktualnej lokalizacji magazynowej,
* podgląd historii zmian lokalizacji.

### Zmiana lokalizacji

* odczyt bieżącej lokalizacji produktu,
* przypisanie nowej lokalizacji,
* automatyczny zapis historii zmian.

### Konfiguracja urządzenia

* konfiguracja identyfikatora urządzenia (Device ID),
* konfiguracja tokenów autoryzacyjnych,
* zapis ustawień lokalnych w przeglądarce.

### Progressive Web App

* możliwość instalacji na urządzeniach mobilnych,
* działanie w przeglądarce internetowej,
* obsługa pliku manifest oraz Service Worker.

---

## Wykorzystane technologie

### Frontend

* HTML5
* CSS3
* JavaScript (Vanilla JS)

### Backend

* Google Apps Script

### Baza danych

* Google Sheets

### Hosting

* GitHub Pages

---

## Struktura projektu

```text
.
├── index.html
├── main.js
├── manifest.json
├── service-worker.js
├── JSONP_Code.gs
├── Magazyn.xlsx
└── README.md
```

---

## Struktura arkusza Google

Projekt wykorzystuje następujące arkusze:

### Magazyn

Przechowuje informacje o produktach i ich aktualnych lokalizacjach.

### HistoriaZmian

Przechowuje historię wszystkich wykonanych zmian lokalizacji.

### Uzytkownicy

Lista użytkowników dostępnych w systemie.

### AktywniUzytkownicy

Rejestr aktualnie aktywnych użytkowników.

### Autoryzacje

Lista autoryzowanych urządzeń wraz z tokenami.

---

## Instalacja backendu

1. Utwórz nowy Arkusz Google.
2. Dodaj wymagane zakładki:

   * Magazyn
   * HistoriaZmian
   * Uzytkownicy
   * AktywniUzytkownicy
   * Autoryzacje
3. Otwórz Google Apps Script.
4. Wklej zawartość pliku `JSONP_Code.gs`.
5. Opublikuj projekt jako Web App.
6. Skopiuj adres URL wdrożenia.

---

## Konfiguracja aplikacji

1. Otwórz aplikację.
2. Wejdź do sekcji „Ustawienia”.
3. Wprowadź:

   * Device ID,
   * Token 1,
   * Token 2.
4. Zapisz konfigurację.

---

## Uruchomienie

### Lokalnie

Wystarczy otworzyć plik:

```text
index.html
```

lub uruchomić projekt przy pomocy lokalnego serwera HTTP.

### GitHub Pages

Aplikacja może zostać opublikowana za pomocą GitHub Pages:

```text
Settings → Pages → Deploy from Branch
```

Po publikacji aplikacja będzie dostępna pod adresem:

```text
https://twoj-login.github.io/nazwa-repozytorium/
```

---

## Wersja demonstracyjna

Repozytorium zawiera przykładowy arkusz danych (`Magazyn.xlsx`), który umożliwia szybkie uruchomienie projektu bez konieczności tworzenia własnej bazy danych.

---

## Autor

Pandinox

Projekt wykonany w ramach zajęć akademickich oraz rozwijany jako praktyczne narzędzie wspomagające pracę magazynową.
