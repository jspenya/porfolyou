# Jose Stephen A. Peña — Developer Portfolio

A production-ready Jekyll portfolio built for GitHub Pages.

## Local Development

### Prerequisites

- Ruby 3.x
- Bundler

### Setup

```bash
cd portfolio
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000` in your browser.

---

## Deploy to GitHub Pages

### Option A — User/Organization site (`username.github.io`)

1. Create a GitHub repo named exactly `jspenya.github.io`.
2. Push this folder's contents to the `main` branch:

```bash
git init
git add .
git commit -m "Initial portfolio"
git remote add origin https://github.com/jspenya/jspenya.github.io.git
git push -u origin main
```

3. Go to **Settings → Pages → Source: Deploy from a branch → Branch: main / (root)**.
4. Your site will be live at `https://jspenya.github.io` within 60 seconds.

### Option B — Project site (any repo name)

1. Create any public repo, e.g. `portfolio`.
2. Push this folder's contents to the `main` branch.
3. Go to **Settings → Pages → Source: Deploy from a branch → Branch: main / (root)**.
4. Update `baseurl` in `_config.yml` to match your repo name:

```yaml
baseurl: "/portfolio"
```

5. Your site will be live at `https://jspenya.github.io/portfolio`.

---

## Project Structure

```
portfolio/
├── _config.yml              # Site configuration
├── index.html               # Main page (pulls in all sections)
├── Gemfile                  # Ruby dependencies
├── _layouts/
│   └── default.html         # Base HTML layout
├── _includes/
│   ├── nav.html             # Navigation bar
│   ├── footer.html          # Footer
│   ├── hero.html            # Hero section
│   ├── about.html           # About section
│   ├── experience.html      # Work experience timeline
│   ├── freelance.html       # Freelance project cards
│   ├── skills.html          # Skills grouped by category
│   ├── education.html       # Education
│   ├── volunteering.html    # Volunteering
│   ├── code_snippet.html    # Rails code example
│   └── contact.html         # Contact links
├── _data/
│   ├── experience.yml       # Employment history
│   ├── freelance.yml        # Freelance projects
│   └── skills.yml           # Technical skills by group
└── assets/
    └── css/
        └── style.scss       # Full design system (BEM, dark theme)
```
