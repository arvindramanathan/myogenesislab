# Ramanathan Lab website

Source for **[myogenesislab.com](https://myogenesislab.com)** — the website of the
Ramanathan Lab at inStem, Bangalore. Built with [Quarto](https://quarto.org).

## How the site is published

Every push to `main` triggers `.github/workflows/publish.yml`, which renders the
site with Quarto and deploys it to GitHub Pages. There is no manual build step.
The `CNAME` file holds the custom domain and must not be deleted.

## Editing

Pages are Quarto markdown (`.qmd`):

| What | Where |
| --- | --- |
| Home, About, People, News, Contact, Platforms | `*.qmd` in the root |
| Research areas | `research/` |
| Individual projects | `projects/` |
| Publication entries | `pubs/` |
| Images | `assets/` |
| Site navigation and settings | `_quarto.yml` |
| Colours, type and layout | `theme.scss` |

Small corrections can be made in GitHub with the pencil button. Keep the YAML
block at the top of each page intact. For anything larger, work on a branch and
open a pull request, so the rendered result can be checked before it is live.

Note that HTML comments in a `.qmd` file are served to the browser and are
readable in View Source. Editorial notes belong outside this repository.

## Working locally

```bash
quarto preview   # live preview at localhost
quarto render    # build into dist/
```

Neither command publishes anything. `dist/` and `.quarto/` are ignored by Git.

## Images and people

`assets/PROVENANCE.md` records the source, credit and consent status of every
photograph on the site. Add a row there before adding an image, and do not
publish a photograph of an identifiable person without their agreement.
