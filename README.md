# Fotokita

A playful browser-based photobooth that lets you snap a 4-photo strip with a live camera preview, styling filters, and a downloadable keepsake.

## Overview

Fotokita is a lightweight static web app built with HTML, CSS, and vanilla JavaScript. It gives you a retro photobooth experience directly in the browser: turn on your camera, choose a mood and frame, take four shots, and download the finished strip as a PNG.

## Features

- Live camera preview with permission handling
- 3-second countdown before each shot
- Four-photo strip layout with a retro booth aesthetic
- Multiple photo filters: Original, Warm, Classic film, Soft portrait, Golden hour, and Black & White
- Multiple strip frames: Classic, Polaroid, and Midnight
- Downloadable photo strip saved locally to your device
- Vercel Web Analytics page-view tracking
- Photos stay in the browser and are never uploaded

## Tech Stack

- HTML5
- CSS3
- JavaScript (vanilla)
- Vercel Web Analytics

## Project Structure

```text
photobooth/
├── app.js         # Camera controls, capture logic, filters, and download flow
├── index.html     # Photobooth markup and UI structure
├── styles.css     # Visual design and booth styling
└── README.md      # Project documentation
```

## Getting Started

Because the app uses the browser camera, it should be served from a local web server or localhost to avoid permission issues.

### Option 1: VS Code Live Server

Open the project in VS Code and launch it with a local static server extension such as Live Server.

## Enable Vercel Web Analytics

This project is plain HTML, so use Vercel's HTML integration rather than installing the React/Next.js package:

1. In your Vercel project dashboard, open **Analytics** and enable Web Analytics.
2. Deploy the site to Vercel and copy the script URL from Vercel's HTML instructions.
3. Paste that URL (for example, `/<unique-path>/script.js`) into the `vercel-analytics-script` meta tag in `index.html`.
4. Deploy again. Page views will appear in the Vercel Analytics dashboard.

The footer keeps its decorative stats UI, but Vercel reports totals in its dashboard rather than exposing them to the page. The displayed dashes are placeholders, not live counts. A successful camera start is also sent as a `Booth Started` custom event; custom events require a Vercel plan that supports them.

See the [Vercel Analytics quickstart for plain HTML](https://vercel.com/docs/analytics/quickstart?framework=html) and the [custom events guide](https://vercel.com/docs/analytics/custom-events) for details.

## How to Use

1. Open the app in a browser.
2. Click "Turn on camera".
3. Allow camera access when prompted.
4. Choose a filter and frame.
5. Click "Take a photo" to capture each shot.
6. Continue until you have taken 4 photos.
7. Click "Download strip" to save the final strip as a PNG.

## Notes

- Camera access is browser-dependent and works best on localhost or HTTPS.
- Photos are processed and downloaded in the browser; they are not uploaded anywhere.
- Analytics requires the site to be deployed on Vercel and enabled in the project dashboard.
- The photobooth itself remains a static, browser-only app; analytics does not upload photos.

## License

This project is provided as-is for personal or demo use.
