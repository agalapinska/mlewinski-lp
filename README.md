# Maciej Lewiński — Pimp My Analytics (landing)

Landing newslettera **Pimp My Analytics** (Maciej Lewiński) — samodzielny, responsywny HTML.

## Struktura repo
- [`index.html`](index.html) — **jedyne źródło deployu**. Odwzorowanie 1:1 projektu Paper **„PMA Landing"** (`PimpMyAnalytics — Landing (v2)`, node `2CR-0`). Vanilla HTML/CSS: pełnoszerokościowe pasy kolorystyczne + kontener treści `max-width:1440px`, płynna typografia `clamp()`, breakpointy 1100 / 900 / 768. Sekcje: header, hero (highlight „zanim zrobią to inni"), social proof, „Cześć, jestem Maciek", „Trzy pytania" (3 karty + „+1"), czarna „Zobacz przykładowe tematy" (cytaty + zapis), opinie (żółte), „Nie wiesz czy to dla Ciebie" (tak/nie), „Marketing się zmienia" + karta „Psst, z Poznania" + kroki 1-2-3, czarna oferta (Newsletter/Kurs/Konsultacje/Szkolenia) + „Poznaj pełną ofertę", stopka z sygnetem ML.
- [`home.html`](home.html) — **poprzednia** strona główna (agencyjny „Homepage-index" z Claude Design). Zachowana; nie jest podpięta pod deploy root.
- [`assets/`](assets/) — grafiki i ikony: `logo.svg`, `sygnet.svg` (monogram ML), `maciek-mailstack.jpg` (foto autora), `avatar-1/2.jpg` (avatary subskrybentów), `icon-mail-eq.svg` (=✉), `ikona-*.svg` (ikony oferty), `logo-*` (loga klientów — placeholder), `linkedin.svg`, `x.svg`.

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
