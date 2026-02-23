# Event Organizer

Configurable event organizer for group get-togethers. Combines date-finding with food/drink preference collection in a single-page app deployed on GitHub Pages.

## Features

- Admin configurable via `?admin` URL parameter
- Built-in templates: Pizza-Abend, Burger-Abend, Film-Abend, Nur Termin, Eigene
- Weekday date grid (Mon-Fri) for availability polling
- Food, drink, and snack preference collection (each category toggleable)
- Automatic pizza/drink quantity calculations with configurable rules
- Results dashboard with date ranking, food/drink breakdowns, participant list
- Returning voter detection (localStorage)
- Print-friendly admin view

## Setup

1. Create a bin at [jsonbin.io](https://jsonbin.io) with initial content `{"config": null, "responses": []}`
2. Set the bin ID in `index.html` (`BIN_ID` constant)
3. Add your JSONBin API key as a GitHub repository secret named `JSONBIN_API_KEY`
4. Push to `main` -- GitHub Actions will inject the key and deploy to Pages

## Usage

- **Admin**: Open `https://<user>.github.io/pizza-poll/?admin` to configure the event
- **Users**: Share `https://<user>.github.io/pizza-poll/` for voting

## Security

The JSONBin API key is injected at deploy time via GitHub Actions secrets. The placeholder `__JSONBIN_API_KEY__` in source is replaced during the CI build. The key never appears in committed source code.

## Deployment

Automatic via `.github/workflows/deploy.yml` on push to `main`. Requires:
- GitHub Pages enabled (Settings > Pages > Source: GitHub Actions)
- Repository secret `JSONBIN_API_KEY` set
