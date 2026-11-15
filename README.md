# BITM-PYQs Downloader

A lightweight, GitHub Pages-compatible website for checking and downloading BIT Mesra previous-year question papers by subject.

## Features

- Search subjects by code or name, or choose from the subject list.
- Generates candidate paper URLs for the selected subject.
- Checks each candidate for a real PDF response before listing it.
- Displays only verified PDFs under **Available question papers**.
- Downloads verified PDFs in the page without opening a new tab for every paper.
- Includes the four supplied EC257 links on the `archive.bitmesra.ac.in` host.
- No backend, database, build step, or local server is required.

## Deploy on GitHub Pages

1. Keep `index.html`, `bitlogo.png`, `README.md`, and `LICENSE` in the repository root.
2. Push the files to your GitHub repository.
3. In **Settings → Pages**, select the branch and root (`/`) folder, then save.
4. Open the published GitHub Pages URL.

You can also test it by opening `index.html` in a modern browser, but browser security policies may behave differently for local files.

## How the availability check works

When the user clicks **Check availability & download PDFs**, the page requests each candidate URL sequentially. It verifies the HTTP response and checks the first bytes for the `%PDF-` signature. Only verified PDF responses are shown in the available-paper list and passed to the download routine. Downloads use in-memory Blob URLs, so the website does not need to open a separate tab for each paper.

## Important GitHub Pages / browser limitation

This project is intentionally static and has no server-side proxy. The browser can inspect a PDF hosted on another domain only if that domain permits cross-origin requests (CORS) from the GitHub Pages origin. If `archive.bitmesra.ac.in` does not permit CORS, the browser will block the response; JavaScript cannot reliably tell whether the remote file exists or inspect its PDF signature. In that case the page reports that verification was blocked and does not claim the files are missing or download unverified URLs.

Browsers may also limit multiple automatic downloads. The user may need to allow multiple downloads for the GitHub Pages site. The page reports that download requests were started; it cannot confirm that the browser saved each file to disk.

## EC257 — Electromagnetic Fields and Waves

The project uses the supplied archive-host links:

- Spring 2023 — End Semester
- Spring 2023 — Mid Semester
- Spring 2022 — End Semester
- Spring 2020 — Mid Semester

The URLs are defined directly in `index.html` and use `https://archive.bitmesra.ac.in/`.

## Project files

```text
BITM-PYQs/
├── index.html    # Complete static website and downloader logic
├── bitlogo.png  # BIT Mesra logo and favicon
├── README.md    # Project documentation
└── LICENSE      # MIT License
```

## Technology

- HTML5
- Tailwind CSS (loaded from its CDN)
- Vanilla JavaScript (Fetch API, Blob, and object URLs)
- GitHub Pages

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
