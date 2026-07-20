# A Paris Story — a visual 5-day itinerary

A self-contained, mobile-friendly Paris itinerary (30 Jul – 3 Aug 2026), hosted on
GitHub Pages. Open it on your phone, share the link, and edit it from anywhere.

## 🌍 Live site

Once Pages finishes its first build, the itinerary is live at:

**https://madhavms.github.io/paris-itinerary/**

(Every push to `main` re-deploys automatically via GitHub Actions — usually live within a minute.)

## 📁 What's in here

| File | What it is | Edit it? |
|------|------------|----------|
| `index.html` | The whole itinerary — layout, styling, and all the day-by-day **content** (in the `DAYS` data near the bottom of the file). ~48 KB, quick to open. | ✅ This is the one to edit. |
| `images.js` | The 16 landmark photos, embedded as data. ~2.6 MB. | ⛔ Rarely — only to swap a photo. |
| `.github/workflows/deploy.yml` | Auto-publishes to GitHub Pages on every push. | ⛔ Leave as-is. |

## ✏️ Making changes (including from your phone)

All the trip content lives in the `DAYS` array inside `index.html`. Each stop looks like:

```js
{ time:"09:00", kind:"Museum", img:"pyramid", name:"The Louvre",
  lede:"…description…",
  meta:[["Hours","09:00–18:00"], ["Ticket","€22"]],
  tips:["…", ["warn","…a warning tip…"]],
  chips:[["book","Book timed entry","https://…"]] }
```

To change something, just ask Claude (e.g. in the Claude app on your phone):

> "In my `paris-itinerary` repo, set the Friday photoshoot time to 06:15 and location to Trocadéro."

Claude edits `index.html`, commits, and pushes — GitHub Actions redeploys, and the live
link updates on everyone's phone within a minute. Refresh the page to see it.

### Available photo keys for `img:`
`trocadero`, `eiffel`, `arc`, `champs`, `concorde`, `louvre`, `pyramid`, `tuileries`,
`orsay`, `saintgermain`, `montmartre`, `notredame`, `saintechapelle`, `marais`,
`versailles`, `seine`

## Notes

- Prices & hours reflect 2026 published rates — reconfirm on official sites when booking.
- The design adapts to light/dark mode and has a theme toggle in the top nav.
- Photos courtesy of Wikimedia Commons contributors.
