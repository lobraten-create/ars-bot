# Arcs Bot — Netlify-driftsättning

## Vad du behöver

- Gratis konto på https://github.com
- Gratis konto på https://netlify.com
- Anthropic API-nyckel från https://console.anthropic.com

---

## Steg 1 — Ladda upp till GitHub

1. Gå till https://github.com/new
2. Skapa ett nytt repo, t.ex. `arcs-bot`
3. Ladda upp hela den här mappens innehåll (index.html, netlify.toml, netlify/functions/ask.js)

---

## Steg 2 — Koppla till Netlify

1. Gå till https://app.netlify.com
2. Klicka **Add new site → Import an existing project**
3. Välj GitHub och välj ditt `arcs-bot`-repo
4. Lämna build-inställningarna tomma — klicka **Deploy site**

---

## Steg 3 — Lägg in API-nyckeln

1. I Netlify, gå till **Site settings → Environment variables**
2. Klicka **Add a variable**
3. Key: `ANTHROPIC_API_KEY`
4. Value: din nyckel från console.anthropic.com (börjar med `sk-ant-...`)
5. Klicka **Save** — Netlify driftsätter om automatiskt

---

## Klart

Din app är nu live på en URL som ser ut ungefär så här:
`https://ditt-namn.netlify.app`

API-nyckeln är aldrig synlig för besökare — den körs bara server-side i Netlify-funktionen.

---

## Kostnad

Anthropic API: Claude Sonnet kostar ca $3 per miljon input-tokens.
Ett botdrag använder ~1 000–2 000 tokens. Räkna med ungefär en krona för 50–100 drag.

Netlify: gratisnivån räcker gott för privat användning.
