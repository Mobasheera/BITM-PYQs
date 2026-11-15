# BITM-PYQs Downloader

A static website for opening previous-year question papers by subject.

## Features
- Subject dropdown and live subject search.
- Opens all configured paper links for the selected subject in separate tabs.
- Displays the papers for which an open/download request was initiated.
- EC257 uses the exact `archive.bitmesra.ac.in` PDF URLs supplied for Spring 2020, Spring 2022 and Spring 2023.

## Important browser limitation
The website cannot reliably confirm that a cross-origin PDF has finished downloading. The archive server and browser decide whether a PDF is downloaded or displayed in a tab. Browsers may block multiple tabs; allow pop-ups for this site if needed. The status list therefore reports links opened/download requests initiated, not verified completed downloads.

## Run
Open `index.html` in a browser or deploy the folder as a static site.
