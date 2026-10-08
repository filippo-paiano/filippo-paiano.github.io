# Personal academic page

Static Jekyll site with no external theme and no JavaScript. GitHub Pages builds it natively.

## Where to edit

| What | File |
|---|---|
| Name, position, affiliation, links | `_config.yml` |
| Home text | `index.md` |
| Publications | `_data/publications.yml` |
| Talks, organization, teaching, projects | `_data/activities.yml` |
| Short CV | `cv/index.md` |
| Full CV (PDF) | `assets/cv.pdf` |
| Style | `assets/style.css` |

## Publishing

Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
The site will be at https://filippo-paiano.github.io/.

## Local preview

    gem install jekyll
    jekyll serve
