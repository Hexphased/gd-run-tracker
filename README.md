# GD run tracker

A small personal page for tracking hard Geometry Dash levels. Each level gets a card with its stats, notes, and a run bar showing which parts of the level I've reached. Click a slice of the bar to open the video for that run.

Where runs overlap, the bar splits into one stripe per run. There is a dark (maroon) and a light (peach) theme, switchable with the button at the top.

## Files

- `index.html` - the main page (level cards)
- `bar.html` - an earlier, bar-only version
- `prototype.html` - the first prototype (run log)

Everything is plain HTML, CSS and JavaScript in one file each. No build step.

## Editing

Open `index.html` and find the `LEVELS` list near the bottom. Each level has a `runs` list:

```js
{ start: 13, end: 88, url: "https://youtu.be/...", note: "What happened" }
```

- `start` / `end` are percentages.
- `url` is an unlisted video link, or `""` for none. Add `?t=123` to start a YouTube clip at a timestamp.
- Set `beaten: true` on a level to unlock its thumbnail.

Stats (rank, list points, GDDL tier) are a snapshot copied from AREDL, so they go out of date.

## Hosting

Enable GitHub Pages in the repo settings (Settings, then Pages, deploy from the main branch). The site then opens at `https://<username>.github.io/<repo>/`.
