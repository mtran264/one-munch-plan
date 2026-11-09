# One Munch Plan

One Munch Plan is a responsive web application with a mobile-first approach meal planner for home cooks. Track what's in your kitchen, save your recipes, plan the week, build a shopping list from what's missing, and log how each meal went.

Current version: **1.0.0**

---

## Features

- **Home:** today's lineup, expiring-item alerts, "Use it up" recipe suggestions, and an "Update status" button once a planned meal's time has passed.
- **Storage:** track fridge, freezer, and pantry items with optional expiry dates, store names, and photos.
- **Recipes:** add, edit, and delete recipes with photos, effort levels, servings, ingredients, and steps. Search and sort, with compact or full-size cards.
- **Plan:** a week view (Sunday or Monday start) with Breakfast, Lunch, and Dinner slots. Pick a recipe in one tap, or log a dish you ate out.
- **Shop:** a grocery list grouped by store section. Mark items as bought, then move them into Storage. Reorder sections and add custom items.
- **History:** every meal with its status (Cooked, Skipped, Eat out, or Not yet), star rating, and filters by week, month, year, or all time.
- **Backups:** export your data and photos to a dated JSON file, and import it later. The app reminds you to back up after 3 meals or recipes, then every 7 days when there are changes.
- **Guided tour:** a short walkthrough on first visit, which you can replay from Settings.
- **Installable:** add the app to your phone's home screen.
- **Update check:** the app reads `version.json` and offers to update when a newer version is published.

---

## Fonts

The app uses three Google Fonts, self-hosted in `fonts/` so no request goes to Google:

| Font | Weights | Used for |
|---|---|---|
| Bricolage Grotesque | 400, 700, 800 | Headings and sheet titles |
| DM Sans | 400, 500, 700 | Body text, buttons, and labels |
| Space Mono | 500, 700 | Small monospace labels and the footer |

Font licenses: all three are available under the SIL Open Font License from [Google Fonts](https://fonts.google.com).

---

## Data and privacy

- All data stays in the browser on the device that uses the app. Nothing is sent to a server.
- Recipes, Storage items, meal plan, shopping list, and history are saved in IndexedDB.
- Photos are compressed in the browser (WebP, or JPEG as a fallback) and cropped to a 4:3 ratio for recipes or a square for Storage items.
- Clearing site data in the browser removes the app's data. Export a backup first.
- Backup files are plain JSON and include photos as embedded images.

---

## Backups

- **Export:** Settings → Export backup. The file is named `one-munch-plan-backup-YYYY-MM-DD.json`.
- **Import:** Settings → Import. Choose "merge" to add to your current data, or "replace" to overwrite it.
- **Clear data:** Settings → Clear data. Use this only after exporting a backup.

---

## Browser support

Current versions of Safari (iOS and macOS), Chrome, Edge, and Firefox. The app uses IndexedDB, CSS grid and flexbox, and `createImageBitmap` for photo handling.

---

## Roadmap

- Service worker for offline use and reliable updates
- Week navigation in the Plan screen
- Quantity scaling when servings change
- Optional push reminders

---