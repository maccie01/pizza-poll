# Pizza Poll

Pizza and drinks preference collection for get-togethers.

## Live URL

- **User View:** https://maccie01.github.io/pizza-poll/
- **Admin View:** https://maccie01.github.io/pizza-poll/?admin=1

## Features

- Name input
- Pizza preference (Vegetarian / Standard / Both OK)
- Multiple drink selection (Cola, Fanta, Sprite, Wasser, Apfelschorle, Bier, Spezi, Eistee)
- Optional dietary restrictions/allergies
- Admin view with:
  - Total participants count
  - Recommended pizza quantities (with buffer)
  - Drink volume calculations
  - Participant list with preferences

## Storage

Currently uses **localStorage** for data persistence. To enable cloud storage (cross-device sync):

1. Go to [jsonbin.io](https://jsonbin.io)
2. Create account / Login
3. Create a new bin with content: `{"responses":[]}`
4. Copy the Bin ID from the URL
5. Update `index.html` line ~590: replace `PLACEHOLDER_BIN_ID` with your bin ID
6. Ensure your Access Key has read+update permissions

## Research Data Used

- **Pizza:** 2-3 slices per person, 8 slices per pizza, 15% buffer
- **Drinks:** ~1.5L per person total

## Porsche Design System

Styled with black/white/gray palette, Inter font, sharp edges, minimalist aesthetic.
