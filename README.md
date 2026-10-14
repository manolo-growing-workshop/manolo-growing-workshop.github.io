# MANOLO Workshop on Growing Neural Networks — website

Static site built with [Hugo](https://gohugo.io/) (v0.145, extended) and deployed to GitHub Pages.

## Editing

Most updates are one-line edits to a data file. You don't need to touch the templates.

| To change…                                   | Edit                                   |
|----------------------------------------------|----------------------------------------|
| Workshop date, tagline, contact emails       | `hugo.toml` → `[params]`               |
| Registration / abstract submission links     | `hugo.toml` → `registration_url`, `submission_url` (while `"#"`, buttons show "opens soon") |
| Important dates (and "tentative" flags)      | `data/dates.yaml`                      |
| Programme / schedule                         | `data/schedule.yaml`                   |
| Invited speakers (and number still TBA)      | `data/speakers.yaml`                   |
| Organizers                                   | `data/organizers.yaml`                 |
| Background reading                           | `data/references.yaml`                 |
| Footer logos                                 | `data/logos.yaml` + image files in `static/img/` |
| Page text                                    | `content/*.md`                         |

To add a confirmed speaker, add them to `data/speakers.yaml` and lower `tba` by one. Then set
`speaker: <key>` on their slot in `data/schedule.yaml`.

In page text, cite a reference with `{{< cite "evci2022" >}}` (keys come from `data/references.yaml`).

Logos: drop `eu-funded.png` (the official "Funded by the European Union" emblem), `inria.png` and
`lisn.png` into `static/img/`. Until a file exists, its name is shown as text instead.

## Preview locally

```bash
hugo server
```

Then open http://localhost:1313/.

## Deploy

Pushing to `main` builds and publishes the site via `.github/workflows/hugo.yml`.
One-time setup on GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
The base URL is set automatically. For a custom domain, set it under Settings → Pages as well.
