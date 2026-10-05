# Student Productivity Dashboard

A small, single-file web app built as a vibe coding assignment. It helps students manage tasks, plan a weekly schedule, keep notes, and practise writing better AI prompts with the CRAFT framework.

No frameworks, no build step, no dependencies. Everything lives in `index.html`.

## Features

- **Tasks:** create tasks with a title and details, open them with "read more", mark them done, or delete them.
- **Schedule:** add events by day and time. They are sorted automatically from Monday to Sunday.
- **Notes:** save short notes and read them in a pop-up.
- **Prompt Lab:** build a prompt from the CRAFT framework (Context, Role, Action, Format, Target) plus Constraints, then copy it. An "explain first" toggle adds an instruction asking the AI to explain its approach before writing code.
- **Progress counter:** the header shows tasks completed, schedule items, and notes.
- **Persistent data:** everything is saved in the browser's `localStorage`, so it survives a refresh.
- **Responsive and accessible:** works on phones, supports keyboard navigation, and respects reduced-motion settings.

## Run locally

1. Download `index.html`.
2. Double-click it to open in any modern browser.

Or serve it on a local port:

```bash
python3 -m http.server 9000
```

Then visit `http://localhost:9000`.

## Deploy

Because it is a single static file, any static host works.

**GitHub Pages**
1. Create a repository and upload `index.html` (and this README).
2. Go to Settings > Pages, choose the `main` branch and the root folder, then save.
3. Your site will be live at `https://<username>.github.io/<repo>/`.

**Netlify**
1. Go to app.netlify.com/drop.
2. Drag the folder containing `index.html` onto the page.

**Vercel**
1. Install the CLI with `npm i -g vercel`.
2. Run `vercel` inside the project folder and follow the prompts.

## Project structure

```
.
├── index.html   # HTML, CSS and JavaScript in one file
└── README.md
```

## How it was built (vibe coding workflow)

The project follows the build loop from the Day 1 session:

**Idea > Prompt > Code > Test > Iterate > Product**

Prompts were written with the CRAFT framework from the Prompt Engineering & Frontend Design session:

| Letter | Part | Example used |
| --- | --- | --- |
| C | Context | Student productivity dashboard for college students |
| R | Role | Senior frontend developer with strong design taste |
| A | Action | Build a task manager, schedule, notes and progress counter |
| F | Format | One HTML file with CSS and JS inside, short comments |
| T | Target | First-year students, mostly on phones, dark theme |

Constraints were also stated: no extra dependencies and a simple architecture. The AI wrote the code, and the developer reviewed, tested, and owns the result.

## Tech stack

- HTML5 (including the `<dialog>` element)
- CSS3 (custom properties, grid, flexbox)
- Vanilla JavaScript (ES6)
- `localStorage` for saving data

## Known limitations

- Data is stored per browser and per device. Clearing site data erases it.
- There is no login or cloud sync.
- Editing existing tasks, notes, or events is not supported yet. Delete and re-add instead.

## Ideas for next steps

- Edit tasks, notes, and schedule items.
- Add due dates and reminders.
- Add a focus timer to track study sessions.
- Export and import data as JSON.

## Author

Your Name
Your Course / Program
Your Institution

## Acknowledgements

- Day 1: Vibe Coding + AI Tools (Trainer: Sanchit)
- Student Development Program by FOSS Club: Prompt Engineering & Frontend Design with AI (Presented by Nilotpal Deb)
