# Tally

Tap-to-log work hours with breaks and pay, organised by semester. Static app (HTML, CSS, JS), no build step.

## Deploy on GitHub Pages

1. Create a new GitHub repository (for example `tally`).
2. Upload all files (`index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg`, the three `.png` icons and this README) to the repo root.
3. Go to Settings > Pages, set Source to "Deploy from a branch", choose `main` and `/ (root)`, then Save.
4. Open `https://<your-username>.github.io/tally/` after a minute or two.
5. On your phone, use "Add to Home Screen" to install it like an app.

## Using it

- Tap Clock in, Start break, End break and Clock out. The live timer shows net hours (breaks excluded).
- Calendar view colours days: green for weekdays worked, amber for weekends worked, blue for a shift in progress, hatched red for weekdays with no log (only after your first entry in the semester).
- Tap any day to add or fix times, edit breaks, or delete it.
- Table view lists the month with hours and pay totals.
- Create and switch semesters from the top bar. Rename, delete, pay and backup live under the gear icon.
- Pay: set your currency and hourly rate under Settings > Pay. To change your rate later, add the new rate with a start date. Earlier days keep the old rate.

## Updating without losing data

Your data lives in the browser, not in the repo, so replacing the app files does not touch it as long as the address stays the same.

1. Export a backup first (Settings > Export backup).
2. Replace the changed files in the same repo and commit to `main`. Do not rename the repo or change your GitHub username, since that changes the address.
3. Wait a minute for Pages to rebuild, then open the app and refresh (pull to refresh, or close and reopen the installed app).
4. Check that your entries are still there. If anything looks wrong, go to Settings > Automatic snapshots and restore, or import your backup file.

Always open the app from the same place. A home-screen install and a browser tab can keep separate data, and so can different browsers or devices. To move data, export on one and import on the other.

Built-in protection: the storage key never changes, old data is upgraded by migration steps instead of being reset, a snapshot is taken daily and before any upgrade, delete or import (last 7 kept), and the app asks the browser to keep its storage persistent. Snapshots live in the same browser, so they do not replace a backup file.

## Data

Everything is stored in your browser (localStorage). Clearing site data or browser storage cleanup can erase it, so export a backup file regularly (the app reminds you after 2 weeks). Excel export can be added later by writing the same data to CSV or XLSX.
