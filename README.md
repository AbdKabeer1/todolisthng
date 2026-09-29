# Päivä (web version)

This is the version of Päivä built to run on Vercel. It's a single
`index.html` file — no server, no Python, no database.

## How it's different from the Mac version
- Your tasks are saved in **your browser's storage** (localStorage), not in
  a `tasks.json` file. That means:
  - Your tasks stay on whichever device and browser you added them on.
    They won't appear on your phone unless you add them there too.
  - Clearing your browser's site data / history will erase your tasks.
  - There is no login and no account, so nobody else can see your tasks.
- There is **no live sync** with Mac Calendar or Reminders — that only
  works on a real Mac, which Vercel doesn't provide. You can still bring
  events in with **Import .ics** and send your tasks out with
  **Export .ics**.

## Deploying
1. Push this folder to a GitHub repository.
2. In Vercel, "Add New Project" and import that repository.
3. Leave the framework preset as "Other" — no build step is needed.
4. Deploy. Vercel will serve `index.html` at your project's URL.

## Local preview (optional)
You can open `index.html` directly in a browser, or run a tiny local
server first:
```
python3 -m http.server 8000
```
then visit `http://localhost:8000`.
