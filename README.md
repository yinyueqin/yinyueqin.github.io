# yinyueqin.github.io

Personal academic homepage of Yueqin Yin, live at https://yinyueqin.github.io.

Built with the [Config-Driven Academic Website Template](https://github.com/Ironieser/ironieser.github.io) by Sixun Dong (MIT License).

## Where things live

| Path | What to edit |
|------|--------------|
| `config/content.json` | Bio, news, publications (with `tldr`, `featured`, `awards`), experience, education, service |
| `config/roadmap.yaml` | Research Roadmap: phases, groups, filters, and which papers appear (matched by `paper_url`) |
| `config/site.yaml` | SEO / JSON-LD, footer copyright, visitor map (off), optional `blog_comments_server` |
| `config/meta.json` | Template info and Scholar-sync status (generated) |
| `teaser/` | Publication thumbnails (shown at 160×90, 16:9 works best) |
| `images/` | Profile photo and company logos |
| `blog/*.md` | Blog posts (Markdown with front matter) |

`index.html`, `publications.html`, `blog.html`, and `assets/js/blog-data.js` are generated. Do not edit them by hand.

## Update the site

```bash
npm ci            # first time only
npm run build     # validates config/, then regenerates the HTML
npm run serve     # preview at http://localhost:8000
```

GitHub Pages serves the `master` branch as-is, so commit the regenerated HTML together with your config changes:

```bash
git add config/ teaser/ images/ index.html publications.html blog.html assets/js/blog-data.js
git commit -m "Update site"
git push
```

The `Build Website (CI)` workflow only checks that the config still builds; it does not deploy.
