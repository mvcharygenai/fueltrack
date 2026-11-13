# FuelTrack (Android-first PWA)

A lightweight, offline-capable petrol expense and mileage tracker for one vehicle.

## Run locally
Open `index.html` in a browser for a quick preview. Browser storage is local to that browser.

## Install on Android
A PWA must be served from HTTPS (or localhost) to install reliably:
1. Upload the contents of this folder to an HTTPS static host (for example GitHub Pages or Netlify).
2. Open the deployed URL in Chrome on Android.
3. Open Chrome menu -> Install app (or Add to Home screen).
4. Launch FuelTrack from the home screen. It works offline after its first successful load.

## Features
- Add, edit and delete fuel entries
- INR expense tracking, litres and pump rate
- Odometer tracking
- Full-tank-to-full-tank mileage estimates
- Dashboard, monthly spending chart, history
- CSV export and JSON backup/restore
- Offline caching

## Important mileage method
For accurate mileage, consistently mark fills as full tank. The app calculates:
(distance between consecutive full-tank odometer readings) / (litres added at the later full-tank fill).
Partial fills can be recorded, but mileage is not calculated from them. Keep odometer readings consistent and increasing.

## Data and privacy
Entries are stored in the browser's local storage on that device. Clearing browser/site data can erase them. Use Download backup regularly and keep the JSON file somewhere safe. CSV is for spreadsheet analysis.

## Current MVP limitations
- One vehicle only
- No cloud sync or automatic backup
- No automatic location, fuel-station lookup, or odometer reading
- No native APK yet; this is an installable web app (PWA)
