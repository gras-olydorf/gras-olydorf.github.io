# GRAS · Olydorf website

The public page of GRAS (Grünanlagen & Umwelt Ausschuss, Studenten im Olympiazentrum e.V.).
It is a static site served by GitHub Pages: free, no server, nothing to renew.

## Update opening hours, prices or the next event (no coding needed)

1. Open `data/kiosk.json` in this repository and click the pencil icon (Edit).
2. Change the values. Keep the quotes and commas as they are.
   - `openDays`: 0 = Sunday, 1 = Monday … 6 = Saturday
   - `openHour` / `closeHour`: hours in Munich time, e.g. `20` and `21`
   - `event.date`: `YYYY-MM-DD`. When the date has passed, the event card hides itself.
   - `prices[].price`: e.g. `"2,50 €"`. Empty shows "price coming soon".
   - `links`: paste the WhatsApp invite link, the Marketplace address, or a contact link (e.g. `mailto:…`).
3. Click **Commit changes**. The site updates within about a minute.

If the page shows "Could not load the opening hours", the JSON has a typo (usually a missing comma or quote).
Open the file's history, compare with the previous version, and fix it.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The page (design and logic) |
| `data/kiosk.json` | Everything the committee edits |
| `assets/` | Logo and icons |

## Marketplace

`links.marketplace` may point to a separate server. The page checks whether it is reachable;
if not, the button falls back to the WhatsApp community, so a switched-off server never leaves a dead link.

## Handing over

This repository belongs to the GRAS GitHub organization, not to one person.
New committee members: ask a current owner to add you to the organization.
Never put phone numbers or other personal data in this repository: it is public.
