# Mapa projektu PROtek

Najprościej: ekran główny znajduje się w `src/App.tsx`, a logika danych w `src/lib/protek/core.ts`.

```text
protek-dashboard-budow/
├── index.html
├── package.json
├── vite.config.ts
├── tsconfig.json
├── README.md
├── STRUKTURA.md
├── public/
│   ├── protek-logo.svg
│   └── robots.txt
├── .github/
│   └── workflows/
│       └── deploy.yml
└── src/
    ├── main.tsx
    ├── App.tsx
    ├── styles.css
    ├── components/
    │   ├── protek/
    │   │   ├── Admin.tsx
    │   │   ├── CsvImport.tsx
    │   │   ├── EntryDialog.tsx
    │   │   ├── Logo.tsx
    │   │   └── SiteDetail.tsx
    │   └── ui/
    │       ├── button.tsx
    │       ├── dialog.tsx
    │       ├── input.tsx
    │       ├── label.tsx
    │       ├── sonner.tsx
    │       ├── switch.tsx
    │       └── textarea.tsx
    └── lib/
        ├── utils.ts
        └── protek/
            ├── core.ts
            ├── core.test.ts
            └── store.ts
```
