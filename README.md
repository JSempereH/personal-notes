# marp-themes

Personal MARP theme & notes collection for building presentation slides from Markdown.


## Usage

Export any slide deck to a self-contained HTML file:

```bash
npx @marp-team/marp-cli@latest example/example.md \
  --theme themes/dracula-marp.css \
  --html \
  --allow-local-files \
  -o example/example.html
```

Then copy the generated HTML into your website under `assets/slides/`.

### Options

| Flag | Purpose |
|---|---|
| `--theme` | Path to the custom CSS theme |
| `--html` | Allow raw HTML in slides (needed for scripts/iframes) |
| `--allow-local-files` | Allow local images and fonts |
| `-o` | Output path |
| `--watch` | Re-build on save (useful while editing) |

Preview in the browser while editing:

```bash
npx @marp-team/marp-cli@latest example/example.md \
  --theme themes/dracula-marp.css \
  --preview
```

## Slide template

Every `.md` file should start with this frontmatter:

```markdown
---
marp: true
theme: dracula-marp
size: 16:9
paginate: true
---

<!-- _class: title -->

# Slide title
**Your name** · 2026
```

To reduce font size globally for a dense slide deck:

```markdown
---
marp: true
theme: dracula-marp
size: 16:9
paginate: true
style: |
  section { font-size: 22px; }
---
```

## Theme

`dracula-marp.css` follows the same color palette as [javiersempere.com](jsempereh.github.io):

| Token | Color | Usage |
|---|---|---|
| `#bd93f9` | purple | headings, strong, keywords |
| `#8be9fd` | cyan | h3, em, variables |
| `#50fa7b` | green | function names |
| `#f1fa8c` | yellow | strings |
| `#ff79c6` | pink | keywords (`import`, `for`, `def`) |
| `#6272a4` | muted blue | comments |
| `#f8f8f2` | foreground | body text |
| `#18181a` | background | slide background |