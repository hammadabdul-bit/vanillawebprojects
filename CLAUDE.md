# vanillawebprojects

Main repo for the "21 Web Projects With Vanilla JavaScript" course
([course link](https://www.traversymedia.com/20-Vanilla-JavaScript-Projects)):
21 standalone mini-projects, each demonstrating one concept (form
validation, hangman, memory cards, etc.) in plain HTML/CSS/JS, no
frameworks.

## No build step

There's no bundler, package manager, or build config anywhere (no
`package.json`, no webpack/vite config). Every project runs straight from
its raw files in the browser. Don't add npm scripts, bundlers, or
transpilation as it defeats the point of the repo.

## Folder organisation

Each top-level directory is one independent, self-contained project:

```
project-name/
  index.html    # entry point
  script.js     # plus any extra .js files
  style.css
  README.md     # project-specific notes (e.g. API keys needed)
  img/ css/ ... # optional asset subfolders, scoped to that project
```

Projects share no code or dependencies. When working on one, only touch
files inside its own folder.

See the root `readme.md` for the full
table with descriptions and live demo links for current projects.

## Running a project

Open the project's `index.html` directly in a browser:

```
start "hangman/index.html"   # Windows
```

Some projects (`lyrics-search`, `meal-finder`, `exchange-rate`, ...) call
external APIs and may need a key. Check that project's README first. If a
project's `fetch` calls hit CORS issues under `file://`, serve the folder
locally instead:

```
python -m http.server 8000   # then visit localhost:8000
```

## Formatting

Never use em dashes.

## This fork

Personal learning fork. Feature additions and experiments are expected.
Ignore the contribution policy in the root readme, which is the upstream
project's.

Default branch is `master`, not `main`.