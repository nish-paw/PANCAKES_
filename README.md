# RentHub

A web app for students to rent items to each other on campus, built for **CodeSprint, problem P-6: Rent a Thing**.

Browse items by zone and category, pick your dates on a calendar, see the total rent, and get a booking code to show the lender when you collect.

It's one file (`index.html`) of plain HTML, CSS and JavaScript. There's nothing to install and no build step.

## Run it

- **On your computer:** download `index.html` and open it in any browser.
- **On GitHub Pages:** push `index.html` to your repo, then go to **Settings → Pages → Deploy from a branch → `main` / root**.

## What it covers (P-6 requirements)

| Requirement | How RentHub does it |
|---|---|
| Catalog with photos | Item cards with a photo (uploaded or a built-in drawing), name, category and zone |
| Owner details | Owner name, phone and pickup zone in the booking popup |
| Daily rent | Price per day on every card |
| Date calendar | Tap a start day and an end day. Booked days and days the owner blocked can't be picked |
| Filter by zones | Zone buttons: TB-1, TB-2, OIST CAMPUS, OCT, OGM, OGP, BOYS HOSTEL, GIRLS HOSTEL, LIBRARY, CANTEEN |
| Total rent | Number of days × rent per day, updated as you pick dates |
| Booking code | A unique code like `LH-3-K7QX`, with a copy button |

## Features

**Browse**
- Search by item, owner or category
- Category dropdown and sort by price
- Zone filter buttons

**Booking**
- Calendar with booked and blocked days marked
- Total rent shown as you pick dates
- Booking code after you confirm

**My bookings**
- Each booking shows Upcoming, Active or Returned
- Change dates, see the code again, or cancel (tap twice to confirm)

**My listings (the lender's side)**
- List an item: name, category (with an **Other** option), rent, zone (with an **Other** option), phone and photo
- Photos are shrunk before saving so they fit in browser storage
- Block days when you need the item back
- Pause, resume, or delete with the bin icon (tap twice to confirm)

**Contact the lender**
- Phone number with a copy button
- An editable ready-made message, plus a button that opens WhatsApp with it filled in

**Themes**
- Light, dark and system modes. Dark is the default
- Colour themes: **Ember** (black and orange, the default), Black, Ocean, Teal, Indigo, Sunset, Rose and Mango
- Every theme has a gradient background
- Your choice is remembered

## How the code is organised

The script inside `index.html` is split into numbered sections:

1. **Helpers:** dates, saving to storage, pop-up messages
2. **Data:** zones, categories, sample items and item drawings
3. **Views:** draws the Browse, My bookings and My listings pages
4. **Calendar:** one calendar used for booking, changing dates and blocking days
5. **Other popups:** booking code, contact lender, list an item
6. **Buttons:** one click handler for every card and row button
7. **Themes:** light/dark mode and colour palettes, applied as CSS variables

## Data storage

For the demo, everything is saved in the browser with `localStorage`. **Reset demo data** in the footer brings back the sample items.

For a real launch, the next steps would be a database (for example Firebase) and a login for each user.

