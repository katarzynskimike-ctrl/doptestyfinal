# Doskonała Obsługa Pacjenta — 6 testów

Statyczna strona z 6 testami psychometrycznymi. Nie wymaga buildu ani serwera — tylko hosting plików statycznych.

## Pliki

- `index.html` — strona główna (hub z 6 kafelkami testów)
- `test-4-typy-osobowosci.html` — Test 1: DISC, 4 archetypy (33 pytania, ~6 min)
- `test-wiedzy-lekarza.html` — Test 2: Wiedza o 7 Czynnikach + M1–M4 (21 pytań z wyjaśnieniami, ~8 min)
- `test-stylu-menadzera.html` — Test 3: DISC dla menedżera (33 pytania, ~7 min)
- `test-wszechstronnego-przywodztwa.html` — Test 4: Wheel 12 obszarów (18 pytań scenariuszowych, ~4 min)
- `test-komunikacja-pokolenia.html` — Test 5: Komunikacja międzypokoleniowa (21 pytań z wyjaśnieniami, ~8 min)
- `macierz-suwerennosci.html` — Test 6: Macierz Wskaźnika Suwerenności WS = Z × K × S ÷ 100 (15 pytań, ~20 min)
- `test-osobowosci-pacjenta.html` — redirect na test-4-typy-osobowosci.html (backwards compat)
- `vercel.json` — konfiguracja dla Vercela (no build, serve as static)

## Wdrożenie na Vercel

### Opcja A: Nowy projekt — drag & drop (rekomendacja)
1. Wejdź na [vercel.com/new](https://vercel.com/new)
2. Wybierz **„Other"** (zamiast importowania z gita) — Browse → wskaż rozpakowany folder
3. Klik **Deploy** — po 30 sekundach dostaniesz nowy URL

### Opcja B: Nowe repo na GitHubie + Vercel
1. GitHub → **New repository** → np. `dop-testy` → **Add a README**
2. W nowym repo: **Add file → Upload files** → przeciągnij wszystkie pliki → **Commit**
3. Vercel → **Add New → Project → Import** Twoje nowe repo → **Deploy**

### Opcja C: Podmiana w istniejącym repo React
1. **Usuń stare pliki React**: `src/`, `package.json`, `package-lock.json`, `vite.config.js`, `postcss.config.js`, `node_modules/`, `dist/`, stary `vercel.json`
2. Wrzuć wszystkie pliki z tego folderu do roota repo
3. `git add . && git commit -m "static HTML site - 6 testów" && git push`
4. Vercel: **Settings → General → Framework Preset** ustaw na **Other**, **Build Command** wyłącz „Override"
5. **Redeploy bez cache** (Deployments → ... → Redeploy → odznacz „Use existing Build Cache")

## Test lokalny

Otwórz `index.html` w przeglądarce — wszystko działa offline.

---
© Michał Katarzyński · 2026
