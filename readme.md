# Dhruv Garg — Portfolio Website

This is the source for my personal portfolio website, built using **[Quarto](https://quarto.org/)**, **HTML**, and **CSS**.

It showcases my:
- Projects
- Education
- Experience
- Resume
- Contact links

---

## Project Structure

```
├── index.qmd           # Homepage
├── about.qmd           # About Me page
├── projects.qmd        # Listing page for all projects 
├── resume.qmd          # Resume page 
├── education.qmd       # Education and certifications 
├── posts/              # Folder containing individual project pages
│    ├── project1.qmd
│    ├── project2.qmd
│    └── ...
├── images/             # Images (logos, project screenshots, gifs)
├── styles.css          # Custom CSS for layout and design
├── _quarto.yml         # Quarto site configuration
└── README.md           # This file
```

---

## How to Edit or Add Content

### 1. Homepage (`index.qmd`)

- The homepage contains cards for:
  - Projects
  - Education
  - Experience
- **Important**: The "View Education" button links to `education.qmd`.

> To add/change cards on the homepage, edit the `<div class="portfolio-card">` blocks inside `index.qmd`.

---

### 2. Projects (`projects.qmd` + `posts/`)

- `projects.qmd` lists projects automatically if you use the `listing:` feature.
- Each project has a file inside the `posts/` folder.
- Example project file: `posts/retailpulse.qmd`

> To add a new project, create a new `.qmd` inside `posts/` and Quarto will pick it up.

---

### 3. Education (`education.qmd`)

- `education.qmd` uses a **stacked layout** — degrees first, certificates after.
- To add a new degree or certificate:
  1. Copy an `<div class="education-item">` block.
  2. Update the title, organization, year, and description.
  3. (Optional) Add/update logos in `images/`.

---

### 4. Experience (`about.qmd` or future `experience.qmd`)

- Linked to `experience.qmd`.

---

### 5. Styling (`styles.css`)

- Main styling such as:
  - Card layout
  - Section headings
  - Button hover effects
  - Fonts and responsiveness
- Edit `styles.css` to customize the look of cards, sections, or entire site theme.

---

### 6. Site Configuration (`_quarto.yml`)

- Controls the navbar links, site title, theme, and external assets.
- If you add a new major page like `education.qmd` or `experience.qmd`, consider adding it to `_quarto.yml` under `navbar:`.

Example:

```yaml
website:
  navbar:
    left:
      - href: index.qmd
        text: Home
      - href: projects.qmd
        text: Projects
      - href: education.qmd
        text: Education
      - href: resume.qmd
        text: Resume
```

---

## Deployment (GitHub Pages)

To deploy the portfolio:

1. Render the site locally:

```bash
quarto render
```

2. Push changes to GitHub.

3. Enable GitHub Pages:
   - Branch: `gh-pages` (if using `quarto publish gh-pages`)
   - Or use `/docs` folder if manually setting `output-dir: docs` in `_quarto.yml`.

4. Your live website will be at:

```
https://your-username.github.io/your-repo-name/
```

---

## Quick Future Checklist

| Task                           | Reminder |
|:--------------------------------|:---------|
| Adding new project              | Create new `.qmd` inside `posts/` |
| Adding new degree/certificate   | Add new block inside `education.qmd` |
| Adding experience               | Create or update `about.qmd` |
| Updating styles                 | Modify `styles.css` |
| Updating site settings          | Modify `_quarto.yml` |
| Deploy new changes              | `quarto render` + Push to GitHub |

---


