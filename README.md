# Pagina personale accademica

Sito statico Jekyll, senza tema esterno né JavaScript. GitHub Pages lo compila da solo.

## Dove modificare

| Cosa | File |
|---|---|
| Nome, posizione, affiliazione, link | `_config.yml` |
| Presentazione (home) | `index.md` |
| Pubblicazioni | `_data/pubblicazioni.yml` |
| Seminari, didattica, ecc. | `_data/attivita.yml` |
| CV | `cv/index.md` e `assets/cv.pdf` |
| Stile | `assets/style.css` |

## Pubblicazione

Settings → Pages → Source: "Deploy from a branch", branch `main`, cartella `/ (root)`.
Il sito sarà su https://filippo-paiano.github.io/.

## Anteprima locale

    gem install jekyll
    jekyll serve
