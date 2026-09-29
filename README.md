# umbywt.github.io

Il mio sito personale: chi sono, per chi lavoro, i progetti, il curriculum e un modulo per contattarmi.
Online su **https://umbywt.github.io**.

È il progetto di sviluppo web del Master in AI e Agenti AI per il Business (Università Guglielmo Marconi / start2impact).

## Pagine

| File | Cosa contiene |
| --- | --- |
| `index.html` | Presentazione, a chi mi rivolgo, servizi, percorso, competenze |
| `progetti.html` | Progetti in azienda, di formazione e del Master, con filtro per categoria |
| `cv.html` | Curriculum in HTML, con uno stile dedicato alla stampa (Ctrl+P → PDF di 2 pagine) |
| `contatti.html` | Modulo di contatto collegato a Formspree |
| `404.html` | Pagina di errore personalizzata, servita in automatico da GitHub Pages |

## Tecnologie

- **HTML e CSS**, senza JavaScript: menu mobile, filtri dei progetti e avvisi del form funzionano solo con CSS.
- **Bootstrap 5** compilato dai sorgenti SCSS, con i miei colori e il font impostati sulle sue variabili. Uso solo i moduli che servono (griglia, form, card, pulsanti, utility), nessun file JavaScript di Bootstrap.
- **Sass**: variabili, mappe, cicli `@each`, funzioni, mixin miei e mixin di Bootstrap (`button-variant`, `media-breakpoint-up`, `color-mode`).
- **Flexbox** (header, card del pubblico, linea del tempo, footer) e **CSS Grid** (hero, servizi, competenze, griglia dei progetti, CV).
- **Responsive** da 320 px in su, **menu sticky** su tutte le larghezze.
- **Tema scuro** automatico con `prefers-color-scheme`.
- **Open Graph** e Twitter Card su ogni pagina, con un'immagine di anteprima 1200×630.
- **Favicon** in SVG, ICO e PNG (anche per iPhone).
- **Roboto ospitato sul sito**, senza chiamate a Google Fonts.

## Struttura

```
├── index.html, progetti.html, cv.html, contatti.html, 404.html
├── favicon.ico
├── assets/
│   ├── css/style.css        ← CSS compilato (quello che legge il browser)
│   ├── fonts/               ← Roboto in woff2
│   └── img/                 ← foto, favicon, immagine Open Graph
└── scss/
    ├── main.scss            ← punto di ingresso
    ├── abstracts/           ← variabili (anche override di Bootstrap) e mixin
    ├── base/                ← font, custom properties, base, stampa
    ├── layout/              ← header e footer
    ├── components/          ← pulsanti, hero, card, timeline
    └── pages/               ← stili specifici di progetti, cv, contatti
```

## Compilare il CSS

```bash
npm install
npm run build    # compila scss/main.scss in assets/css/style.css
npm run watch    # ricompila a ogni salvataggio
```

GitHub Pages non compila Sass, per questo nel repository c'è anche `assets/css/style.css` già compilato.
