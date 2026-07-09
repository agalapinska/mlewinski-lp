# Maciej Lewiński — Pimp My Analytics (landing)

Statyczna strona główna Maciej Lewiński / Pimp My Analytics.
Odwzorowanie szablonu **Claude Design → `templates/home-page/HomePage.dc.html`**
(projekt „Maciej Lewiński Design System") jako samodzielny, responsywny HTML.

## Struktura repo
- [`index.html`](index.html) — **jedyne źródło deployu**. Vanilla HTML/CSS/JS (logika DC przepisana na czysty JS: mega-menu, scroll-reveal, parallax, licznik wyników, marquee). Responsywne: desktop ≥1440 (1:1 z designem), tablet ≤1439, mobile ≤768.
- [`assets/`](assets/) — grafiki i ikony **wspólne z szablonem** w Claude Design (te same nazwy plików: `hero.jpg`, `wyniki.jpg`, `schody.jpg`, `sygnet.svg`, `ikona-*.svg`, `logo-*`, `subskrybent.jpg`, …).

## Deploy (GitHub Pages)
Źródło: `main` / `/` (root). **Każdy `git push` na `main` auto-redeployuje** (<1 min):
`https://agalapinska.github.io/mlewinski-lp/`

```bash
git add -A && git commit -m "opis zmiany" && git push origin main
```

## Sync z Claude Design
Projekt design-systemu: `Maciej Lewiński Design System`
(id `e1c176ba-5fc3-420b-8b11-e4a0519564f2`).
- Źródło szablonu: `templates/home-page/HomePage.dc.html` (format DC, z runtime).
- Breakpointy responsywne wpięte w szablon przez selektory `data-screen-label` + hook `.om-root` (spójne z tym repo).
- Sync przez DesignSync MCP wymaga logowania `/design-login` w **interaktywnej** sesji `claude`.
- Standalone-export z Claude Design to spakowany bundle (runtime, ekran „Unpacking…") — do publikacji na GitHub służy `index.html` z tego repo, nie bundle.

## Do podmiany przed publikacją produkcyjną
Zdjęcia (hero/wyniki/schody/subskrybent), logo klientów, prawdziwe cytaty w sekcji „Opinie", teksty CTA/oferty, podpięcie mailingu (double opt-in + UTM).
