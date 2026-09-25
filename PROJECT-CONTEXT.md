# Sprout Points Project Context

## Project

Sprout Points is a browser-based kids reward system. Parents or caregivers can create child profiles, award or deduct points, record reasons, redeem points, and view history.

## Main Files

- `index.html`: Complete single-page application, including HTML, CSS, and JavaScript.
- `manifest.json`: Progressive Web App metadata and icon declarations.
- `sw.js`: Service worker for caching and offline support.
- `icons/`: PWA icons used by the manifest.
- `PWA-INSTRUCTIONS.md`: Instructions for launching, installing, backing up, and restoring the PWA.

## Data Storage

The app stores data in the browser's `localStorage` on the current device. It does not use a backend server or automatically synchronize data between devices.

Stored data can include:

- Child names and ages
- Avatars and badges
- Point balances
- Point transaction history
- Reasons and notes
- Timestamps

## Backup and Restore

The Backup feature exports the complete app state to a JSON file named like `sprout-points-backup-YYYY-MM-DD.json`. Restore reads a JSON backup file and replaces the current browser data after confirmation.

Backup files may contain personal information and should be kept private.

## PWA Deployment

The intended public URL is:

https://ashwiniashokshamayatech.github.io/sprout-points/

GitHub Pages must be enabled for the repository's `main` branch before the URL is available. PWA installation requires the app to be served over HTTPS or from localhost.

## Repository

- Remote: `https://github.com/ashwiniashokshamayatech/sprout-points.git`
- Branch: `main`
- Git identity: `ashwiniashokshamayatech@users.noreply.github.com`

## Development Notes

This is a static app and can be opened directly as a local HTML file for basic UI testing. Service worker and install behavior should be tested through an HTTP or HTTPS URL.

When making changes:

1. Update the relevant source file.
2. Test the affected workflow in a browser.
3. Run `git diff --check`.
4. Commit the change on `main`.
5. Push with `git push origin main`.
