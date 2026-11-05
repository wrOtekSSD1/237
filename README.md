[README.md](https://github.com/user-attachments/files/34423336/README.md)
# PROtek — Dashboard Budów

Aplikacja do prowadzenia dziennika prac na budowach. Projekt jest przygotowany do pracy lokalnej oraz publikacji przez GitHub Pages.

## Uruchomienie na komputerze

Wymagany jest Node.js 22 lub nowszy.

```bash
npm install
npm run dev
```

Otwórz adres pokazany w terminalu (zwykle `http://localhost:5173`).

## Budowanie i testy

```bash
npm test       # testy logiki aplikacji
npm run build  # sprawdzenie TypeScript + gotowa strona w katalogu dist/
npm run preview
```

## Publikacja przez GitHub Pages

1. Utwórz repozytorium na GitHubie.
2. Wgraj do niego zawartość tego katalogu (plik `index.html` musi być w katalogu głównym repozytorium).
3. W GitHubie otwórz **Settings → Pages**.
4. W sekcji **Build and deployment** wybierz **GitHub Actions**.
5. Wypchnij zmiany na gałąź `main`. Workflow z katalogu `.github/workflows/` zbuduje i opublikuje stronę.

Po zakończeniu publikacji link do strony będzie widoczny w **Settings → Pages** oraz w zakładce **Actions**.

## Gdzie co zmieniać

| Plik / katalog | Do czego służy |
| --- | --- |
| `index.html` | Tytuł strony, opis, ikona i fonty |
| `src/App.tsx` | Główny ekran, nagłówek, wyszukiwanie i lista budów |
| `src/components/protek/SiteDetail.tsx` | Szczegóły budowy, kalendarz i wpisy |
| `src/components/protek/EntryDialog.tsx` | Formularz dodawania i edycji wpisu |
| `src/components/protek/Admin.tsx` | Panel administracyjny budów |
| `src/components/protek/CsvImport.tsx` | Import plików CSV |
| `src/components/protek/Logo.tsx` | Logo PROtek |
| `src/lib/protek/core.ts` | Dane, reguły, daty, święta, pracownicy i import CSV |
| `src/lib/protek/store.ts` | Zapisywanie danych, widoku i motywu w przeglądarce |
| `src/styles.css` | Kolory, motyw jasny/ciemny i style globalne |
| `public/` | Pliki statyczne, np. logo |

## Ważne o zapisywaniu danych

W tej wersji dane budów i wpisy są zapisywane w `localStorage` przeglądarki. Oznacza to, że:

- dane pozostają na urządzeniu i w przeglądarce, w której je wprowadzono;
- opublikowanie strony udostępnia innym samą aplikację, ale **nie synchronizuje automatycznie ich wpisów**;
- wyczyszczenie danych przeglądarki może usunąć lokalne wpisy — warto regularnie eksportować/kopiować dane.

Jeżeli z aplikacji ma korzystać kilka osób ze wspólną bazą danych, potrzebne będzie podłączenie backendu/bazy (np. Supabase) i ustalenie logowania oraz uprawnień. Nie jest to włączone ani udawane w obecnej wersji.

## Technologie

React, TypeScript, Vite, Tailwind CSS. Nie jest wymagany edytor Lovable ani serwer TanStack Start.
