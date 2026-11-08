# AI Engineering Roadmap

**A four-year, interactive learning roadmap from BSCS foundations to full-stack AI engineering (2026–2030).**

This single-page website brings together a structured learning path, practical projects, skills, certifications, internship preparation, and an example production AI architecture. Follow the stages, explore resources, and track your progress in your own browser.

## Live website

[Explore the AI Engineering Roadmap](https://dawood-0001.github.io/Ai-engineering-roadmap/)

> If the GitHub Pages address changes, update this link accordingly.

## Features

- **Dashboard:** Four-year overview from computer science fundamentals to production AI systems.
- **Interactive roadmap:** 20 stages with detailed learning topics, suggested resources, and completion milestones; filter by year and mark stages complete.
- **Skill tree:** Explore computer science, web development, Python, machine learning, deep learning, generative AI, and production AI skills.
- **Project lab:** Seven project levels, each with a completion toggle.
- **Certification map:** Compare learning resources, course certificates, and professional certifications.
- **Internship roadmap:** Preparation tips for internships and early career development.
- **Architecture overview:** A reference stack for full-stack AI applications and a capstone concept.
- **Search and navigation:** Search roadmap stages, navigate sections, and use `Ctrl+K` (or `Cmd+K`) to focus the search field.
- **Theme toggle:** Switch between dark and light appearance.
- **Local progress saving:** Completion status is saved automatically in the browser.

## Four-year learning journey

| Year | Focus | Example topics |
| --- | --- | --- |
| 1 | Foundations | CS50x, Git, Linux, HTML, CSS, JavaScript, basic DSA |
| 2 | Software engineering | React, TypeScript, Node.js, Express, PostgreSQL, Docker, CI/CD |
| 3 | AI and machine learning | Python, statistics, machine learning, deep learning, PyTorch, LLMs |
| 4 | Full-stack AI engineering | RAG, AI agents, FastAPI, cloud, evaluation, system design |

The roadmap is a suggested sequence, not a guarantee of a job or a substitute for university coursework.

## Tech stack

| Technology | Purpose |
| --- | --- |
| HTML5 | Page structure and content |
| CSS3 | Responsive styling, layout, and themes |
| Vanilla JavaScript | Navigation, filtering, rendering, and interactive controls |
| Web Storage API (`localStorage`) | Browser-side progress and theme persistence |
| GitHub Pages | Static website hosting |

**No backend, database, framework, or build process is required.** CSS and JavaScript are embedded in the HTML file.

## How progress tracking works

The site stores completed roadmap stages and project levels in the visitor's browser using `localStorage`.

When you mark a stage complete, the app updates its JavaScript state and saves it:

```js
function save() {
  localStorage.setItem('aiRoadmapState', JSON.stringify(state));
  updateProgress();
}
```

On page load, it restores the saved state:

```js
const state = JSON.parse(localStorage.getItem('aiRoadmapState') || '{}');
state.done = state.done || {};
state.projects = state.projects || {};
```

The progress indicator is calculated from the number of completed roadmap stages and project levels. The selected theme is stored separately under `aiRoadmapTheme`.

### Data persistence and limitations

- Progress normally remains after refreshing the page, closing the tab, or restarting the browser.
- `localStorage` has no built-in expiration date, but **four-year retention is not guaranteed**.
- Data is specific to the browser profile and website origin. It does **not** automatically sync across devices or browsers.
- Clearing site data, using private browsing, changing the site origin, or browser storage cleanup can remove access to saved progress.
- The current site has **no account system, cloud backup, or export/import feature**.

For long-term tracking, planned improvements include manual progress export/import and optional cloud sync.

## Run locally

1. Download or clone the repository:

   ```bash
   git clone https://github.com/dawood-0001/Ai-engineering-roadmap.git
   ```

2. Open the project folder.
3. Open `index.html` in a modern browser.

No dependencies or installation commands are needed.

## Deploy with GitHub Pages

1. Ensure the homepage is named **`index.html`** and is located in the repository root.
2. Go to **Settings → Pages** in the GitHub repository.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose the `main` branch and `/(root)`, then save.
5. Wait for GitHub Pages to publish the site and open the URL shown in Settings → Pages.

## Project structure

```text
Ai-engineering-roadmap/
├── index.html    # HTML, embedded CSS, and JavaScript
└── README.md     # Project documentation
```

## Planned improvements

- Export and import progress backups as JSON.
- Reset progress with a confirmation prompt.
- Optional sign-in and cloud synchronization across devices.
- Improved accessibility and mobile navigation.
- More direct links to learning resources and project examples.

These are ideas for future development, **not features currently implemented**.

## Author

**David Dennis**

Created as an interactive learning companion for the journey from BSCS to full-stack AI engineering.

## License

No license has been specified for this repository. Add a `LICENSE` file if you decide to grant others permission to reuse or modify the code.
