# CEO Project Dashboard

A single-page portfolio/Gantt dashboard: status stat cards, a draggable
timeline for scheduling projects, click-to-edit bars, and month-by-month
navigation across the Gantt.

## Run it

No build step — it's a single static file.

```bash
open index.html          # macOS
# or just double-click index.html, or serve it:
python3 -m http.server 8000
```

## Structure

- `index.html` — everything (markup, styles, and vanilla JS) in one file.
  Project data lives in the `projects` array and is persisted to the
  browser's `localStorage` (key `ceodb.projects.v1`) on every add, edit,
  and delete, so the dashboard always reflects the latest updates on
  reload — no backend yet.

## Where to take it next

- Swap localStorage for a small backend/API for multi-device access
- Multi-user support / auth
- Drag-to-resize or drag-to-move existing bars (currently: drag-to-create
  on the bottom lane, click-to-edit on existing bars)
- Export/print view
