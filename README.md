# nasimhossain.dev

Personal portfolio site for **Nasim Hossain** — Jr. Software Engineer, RHCSA, 2× ICPC Dhaka Regionalist.

**Live:** [nasimhossain.dev](https://nasimhossain.dev)

---

## Stack

| Layer | Tech |
| --- | --- |
| Generator | [Jekyll](https://jekyllrb.com/) (via `github-pages` gem) |
| Hosting | GitHub Pages + GitHub Actions |
| CSS | Hand-rolled (`assets/css/main.css`) — no framework |
| Fonts | JetBrains Mono (Google Fonts) |
| Icons | Font Awesome 6 |
| Theme | Dark / Light toggle, persisted in `localStorage` |

No Minimal Mistakes. No Bootstrap. Just Jekyll + custom CSS.

---

## Features

- Dark/light mode toggle with zero flash on load
- Responsive two-column layout (sidebar + content)
- Terminal-style hero block
- CI/CD pipeline timeline for experience
- Skill badge groups by category
- Stats cards for competitive programming
- Inline resume (PDF iframe)
- SVG favicon

---

## Local Development

**Prerequisites:** Ruby 3.1+, Bundler

```bash
git clone https://github.com/imnasim31415/imnasim31415.github.io.git
cd imnasim31415.github.io
bundle install
bundle exec jekyll serve --livereload
```

Open [http://localhost:4000](http://localhost:4000).

---

## Structure

```text
.
├── _layouts/
│   ├── default.html      # Full HTML shell (nav, sidebar, footer, scripts)
│   └── single.html       # Pass-through → default (legacy support)
├── _data/
│   └── navigation.yml    # Nav links
├── assets/
│   ├── css/main.css      # All styles
│   ├── images/           # Avatar, favicon.svg
│   └── resume/           # CV PDF
├── _config.yml
├── Gemfile
└── index.md              # Homepage content
```

---

## Deploy

Pushes to `main` automatically trigger the GitHub Actions workflow (`.github/workflows/jekyll.yml`) which builds and deploys to GitHub Pages.
