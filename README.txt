
# Yarn Cost Calculator (Static, No-Build)

This is a standalone HTML app that reproduces the functionality of your Replit-based Yarn Cost Calculator without any server or build tools. It runs entirely in the browser.

## How to use

- Open `yarn-cost-calculator.html` in any browser — it just works.
- Upload to your website hosting (e.g., `public_html/yarn-calculator/`) and link to it.
- WordPress: Add a **Custom HTML** block to a page and paste the contents of `yarn-cost-calculator.html` between `<body> ... </body>` (or use a plugin to upload the file and iframe it).

## Features
- Add yarn entries with price and yardage (name optional)
- Computes **cost per yard**
- Highlights **Best / Average / Expensive** relative to lowest cost
- Summary: Best Value, Average Cost, Total Entries
- Clear All and **Export Results (CSV)**

## Notes
- TailwindCSS is loaded via CDN for styling; no build step required.
- No external network calls; all logic is client-side.
