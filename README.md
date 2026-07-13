# Maciej Lewiński — Pimp My Analytics (landing)

Landing newslettera **Pimp My Analytics** (Maciej Lewiński) — samodzielny, responsywny HTML.

## Struktura repo
- [`index.html`](index.html) — **strona główna (root domeny)**. Hero „Zamieniam w zysk", mega-menu Oferta, żółty panel zapisu „Mierz marketing lepiej. Bez zgadywania." (bez pola imię), czarna sekcja scroll-reveal, oferta (CTA: Umów się na konsultacje / Zapisz się na szkolenie / Zaproś mnie do siebie), wyniki flat z licznikiem, ściana opinii+logotypów na żółtym, karta „Poznańska stopka oszczędnościowa", stopka na `#F7F4EC` z sygnetem ML (bez żółtej kurtyny). Po feedbacku klienta z 2026-07-13. Responsywne: desktop ≥1440, breakpointy 1200/900/768.
- [`newsletter.html`](newsletter.html) — **subpage newslettera** (`/newsletter.html`). Odwzorowanie 1:1 projektu Paper **„PMA Landing"** (`PimpMyAnalytics — Landing (v2)`, node `2CR-0`): hero (highlight „zanim zrobią to inni"), social proof, „Cześć, jestem Maciek", „Trzy pytania", czarna „Zobacz przykładowe tematy", opinie, „Nie wiesz czy to dla Ciebie", karta „Psst, z Poznania" + kroki 1-2-3, czarna oferta, stopka. Logo w nagłówku linkuje do strony głównej.
- [`assets/`](assets/) — grafiki i ikony wspólne dla obu stron: `logo.svg`, `sygnet.svg` (monogram ML), zdjęcia (`hero.jpg`/`wyniki.jpg`/`schody.jpg`/`maciek-mailstack.jpg`), avatary, `ikona-*.svg`, `logo-*` (loga klientów — placeholder), `linkedin.svg`, `x.svg`.

## Paleta (z projektu Paper / KV)
- Żółć primary `#FFC820` (header, highlight hero, „+1", przycisk „Chcę czytać", checki), żółć głęboka `#FEBF00` (opinie, karta „Psst", karty oferty, obwódka avatarów).
- Tło strony `#F9F9F9`, biel `#FFFFFF`, off-white `#FFFEFA`, ink `#15140F` / `#111111`.
- Font: **Inter** (400/500/600/700/800).

## Deploy (GitHub Pages)
Źródło: `main` / `/` (root). **Każdy `git push` na `main` auto-redeployuje** (<1 min):
`https://agalapinska.github.io/mlewinski-lp/`

```bash
git add -A && git commit -m "opis zmiany" && git push origin main
```

## Podgląd lokalny
`python3 -m http.server 4321 --directory .` (config w `.claude/launch.json`, ignorowany w git).

## Do podmiany przed publikacją produkcyjną
Loga klientów (placeholder), prawdziwe cytaty w „Opinie" (obecnie „Firma / Imię, Stanowisko"), podpięcie mailingu (double opt-in + UTM), linki nawigacji/stopki, Regulamin i Polityka Prywatności.
