# Bloc-notes — pubblicazione su GitHub Pages

Pacchetto pronto per la pubblicazione come PWA installabile.

## Contenuto del pacchetto

```
index.html              ← l'app
manifest.json           ← dichiara nome, icone, colori (richiesto per PWA)
sw.js                   ← service worker (cache offline + requisito install)
icon.svg                ← icona vettoriale
icon-180.png            ← apple-touch-icon
icon-192.png            ← Android home screen
icon-512.png            ← splash screen
icon-512-maskable.png   ← icona adattiva Android (con safe zone)
```

---

## Pubblicazione su GitHub Pages — 5 minuti

### 1. Crea un account GitHub (se non l'hai)
Vai su https://github.com/signup → username, email, password. Gratuito.

### 2. Crea un nuovo repository
- Clicca il "+" in alto a destra → **New repository**
- **Repository name**: `blocnotes` (o quello che preferisci)
- **Public** (necessario per GitHub Pages gratis)
- Spunta **Add a README file**
- Clicca **Create repository**

### 3. Carica i file
Nella pagina del repo appena creato:
- Clicca **Add file** → **Upload files**
- Trascina TUTTI i file di questo pacchetto (index.html, manifest.json, sw.js,
  e i 4 file PNG + 1 SVG) nella zona di drop
- Scrivi un messaggio commit, poi **Commit changes**

### 4. Attiva GitHub Pages
- Nel repo, clicca **Settings** (in alto a destra)
- Menu laterale: **Pages**
- Sotto "Build and deployment":
  - Source: **Deploy from a branch**
  - Branch: **main** / **/ (root)** → **Save**
- Aspetta 30–60 secondi. Aggiorna la pagina.
- In cima vedrai: **Your site is live at https://TUONOME.github.io/blocnotes/**

### 5. Apri l'URL sul telefono
- Apri Chrome (Android) o Safari (iPhone)
- Vai all'URL `https://TUONOME.github.io/blocnotes/`
- Dopo qualche secondo Chrome mostrerà un banner "Installa app" oppure:
  - **Android Chrome**: menu ⋮ → **Installa app** (o "Aggiungi a schermata Home")
  - **iPhone Safari**: pulsante Condividi ⎙ → **Aggiungi a schermata Home**

L'icona appare sulla home come una vera app, si apre senza barra del browser,
funziona offline.

---

## Aggiornamenti successivi

Quando vuoi cambiare qualcosa:
1. Vai sul repo GitHub
2. Apri il file da modificare (es. `index.html`)
3. Clicca l'icona matita ✎
4. Modifica e **Commit changes**
5. L'app sul telefono si aggiorna automaticamente al successivo avvio
   (il service worker scarica la nuova versione in background)

---

## Note

- **I tuoi dati (note + allegati) restano nel browser del dispositivo**, non
  vengono caricati su GitHub. Il repo contiene solo l'app vuota.
- **Sincronizzazione tra dispositivi**: non c'è automatica. Usa l'export
  Excel come backup/transfer manuale.
- **Privacy**: il repo è pubblico ma contiene solo il codice. Nessuno può
  vedere le tue note.
- **Repo privato**: GitHub Pages richiede repo public sul piano gratuito.
  Se vuoi privacy totale del codice serve GitHub Pro (4$/mese) oppure
  hosting alternativo (Netlify, Cloudflare Pages — entrambi gratis e
  supportano repo privati).
