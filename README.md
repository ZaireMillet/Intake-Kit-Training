# Outstanding Kit Training Program

Internal training portal for Barasch & McGarry Health Program Claim Administrators.

## What this is
A single self-contained HTML file (`index.html`) — no build step, no server, no dependencies to install. It includes:
- A login screen (name + work email, stored locally per device)
- 5 required training modules + a Cheat Sheet quick-reference (unlocked after completing all 5)
- Knowledge checks throughout each module
- Progress tracking saved in the browser (per person, per device)

## How to update the content
Open `index.html` in a text editor and look for the `MODULES` and `CHEATSHEET` variables inside the `<script>` tag — that's where all the training text, questions, and answers live. Everything else (styling, navigation, login logic) is below/above that data block and shouldn't need to change for routine content edits.

## Hosting
This repo is set up to be served directly via GitHub Pages. See the setup steps provided separately, or in GitHub: **Settings → Pages → set source to the `main` branch, root folder.**

## Notes
- Progress is stored in each visitor's browser (`localStorage`), keyed to the email they log in with. It does not sync across devices and is not visible to anyone else — there's no backend or database involved.
- A standard (free) GitHub Pages site is public to anyone with the link. There's no real access-control login here — the login screen only personalizes the experience and separates progress between people sharing a device.
