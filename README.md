# Jonathan Jayes: blog

Source for [blog.jonathanjayes.com](https://blog.jonathanjayes.com), a Quarto website. It used to live at interludeone.com, which now redirects here path for path.

## Render

```bash
quarto preview          # live reload
quarto render           # full site into docs/
```

Code cells are frozen (`freeze: true`), so a render reuses `_freeze/` and does not need R or Python unless you change a post's code. To re-execute one post, render it on its own: `quarto render posts/<folder>/<file>.qmd`.

## Deploy

A push to `main` renders the site and deploys `docs/` to Firebase Hosting (project `jonathanjayes-com`, site `jonathanjayes-com`). Pull requests get a preview channel. `_redirects` is copied into `docs/` for the old Netlify site and ignored by Firebase.

## Layout

| Path | What |
|---|---|
| `posts/` | One folder per post |
| `content/` | Research, teaching, publications, data pages |
| `assets/` | Theme (`custom.scss`), images, CV PDF |
| `docs/` | Rendered output, committed |
| `_freeze/` | Frozen code output, committed |

The rest of the web presence (home page, talks, projects, Instagram) lives in [j-jayes/jonathanjayes.com](https://github.com/j-jayes/jonathanjayes.com).
