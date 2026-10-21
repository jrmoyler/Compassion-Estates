# Compassion Estates

Booking site for one villa week: The Crown Villas, 7-bedroom villa, Lifestyle Holidays Vacation Club, Cofresí Beach, Puerto Plata, Dominican Republic. Tuesday, December 1 through Tuesday, December 8, 2026 (7 nights). $4,900 for the full week.

Reference: Reservation #1808205 · Ad #511378.

## Pages

A single static page with three views, linked by hash:

- `#estate`: hero, week strip, villa facts, included features, closing call to action
- `#gallery`: the villa (8 photos) and the resort around it (6 photos), with a lightbox
- `#book`: week summary, included, fees and terms, inquiry form, next steps, contact

There is a custom intro loader (an arch draws, the seven nights count up, the pool fills, and the photo flies into the hero frame) and a louvered-shutter transition between views. Both are skipped for visitors who have turned on reduced motion.

## Booking inquiries

Inquiries go to the Timeshares Only booking agents:

- fabiane.f@timesharesonly.com
- vivian.gutierrez@timesharesonly.com

Each inquiry names Reservation #1808205 and the December 1–8, 2026 dates in the subject line and body.

The site has no backend. As shipped, a valid inquiry becomes a ready-to-send email (copy button and `mailto:` link to both agents). To send inquiries directly, set `INQUIRY_ENDPOINT` near the top of the script in `index.html` to a form service endpoint that forwards to both agents. The page then posts the inquiry as JSON and shows the confirmation message, or the failed-send message if the post fails.

The site does not take payment or confirm bookings. No inquiry data is stored.

## Deploy

Static files only, with no build step. Serve the repo root from any static host (Vercel, Netlify, GitHub Pages).

```
python3 -m http.server 8000
```

## Before going public

- Transferability of the December week for a rental
- Fee treatment: whether $4,900 is the week price only or all-in
- Branding: whether The Compassion Hub name and phone stay on the public page
- Gallery: confirm the villa photos show the house assigned to this reservation
- Custom domain
