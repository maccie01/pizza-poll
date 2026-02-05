# Pizza Poll

Pizza and drinks preference collection for 30-person get-togethers.

## Live URLs

- **User View:** https://maccie01.github.io/pizza-poll/
- **Admin View:** https://maccie01.github.io/pizza-poll/?admin=1

## Current Status

**Working with localStorage** - Data persists per browser. For cross-device sync, see "Enable Cloud Storage" below.

## Features

- Name input
- Pizza preference: Vegetarian / Standard / Both OK
- Multiple drink selection: Cola, Fanta, Sprite, Wasser, Apfelschorle, Bier, Spezi, Eistee
- Optional dietary restrictions/allergies field
- **Admin view** (`?admin=1`):
  - Participant count
  - Recommended pizza quantities (with 15% buffer)
  - Drink volume calculations
  - Full participant list
  - Print functionality

## Enable Cloud Storage

To enable data sync across devices:

1. Go to [jsonbin.io](https://jsonbin.io) and sign up/login
2. Click "Create a Bin"
3. Enter content: `{"responses":[]}`
4. Click Create → Copy the Bin ID from the URL
5. Go to Settings → API Keys → Create Access Key (read + update permissions)
6. Edit `index.html` line 646: Replace `'PLACEHOLDER_BIN_ID'` with your bin ID
7. Commit and push the change

## Research Data

- **Pizza:** 2-3 slices/person, 8 slices/pizza, 15% buffer → ~12-14 pizzas for 30 people
- **Drinks:** ~1.5L per person (soft drinks 1L + beer/water 0.5L)

## Design

Porsche Design System: black/white/gray, Inter font, sharp edges, minimalist.
