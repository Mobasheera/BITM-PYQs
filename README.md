# 📚 BITM-PYQs Downloader

> 🔗 [Live Demo on GitHub Pages](https://mobasheera.github.io/BITM-PYQs/)
>
> A lightweight, mobile-friendly website for accessing previous-year question papers from BIT Mesra.

## Features

- Simple subject selector and responsive interface.
- Direct paper links for **EC257 — Electromagnetic Fields and Waves** (four supplied archive PDFs).
- Generates the existing year/session links for the other subjects.
- Opens each selected PDF in a new browser tab, where it can be viewed or downloaded.
- Optional visit and download counters.

## Subjects

- MA107 MATHEMATICS-II
- PH113 PHYSICS
- BE101 BIOLOGICAL SCIENCE FOR ENGINEERS
- CS101 PROGRAMMING FOR PROBLEM SOLVING
- EE101 BASIC OF ELECTRICAL ENGINEERING
- **EC257 ELECTROMAGNETIC FIELDS AND WAVES**

### EC257 papers included

| Examination | Session | PDF |
|---|---|---|
| End Semester | Spring 2023 | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2023%20QP/EC257%20ELECTROMAGNETIC%20FIELDS%20AND%20WAVES%20(END_SP23).pdf) |
| Mid Semester | Spring 2023 | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2023%20QP/EC257%20ELECTROMAGNETIC%20FIELD%20AND%20WAVES%20(MID_SP23).pdf) |
| End Semester | Spring 2022 | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2022%20QP/EC257%20ELECTROMAGNETIC%20FIELDS%20AND%20WAVES%20(END_SP22).pdf) |
| Mid Semester | Spring 2020 | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2020%20QP/EC257%20ELECTROMAGNETIC%20FIELDS%20%26%20WAVES%20(MID_SP20).pdf) |

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a browser, or serve the folder with VS Code Live Server.
3. Select a subject and click **Download PDFs**.
4. Choose the paper link you want to open.

No build step or package installation is required.

## Tech stack

- HTML5
- Tailwind CSS (CDN)
- Vanilla JavaScript
- GitHub Pages

## Notes

- EC257 uses the exact archive URLs supplied for this update, rather than the generic URL generator used for the other listed subjects.
- The other five subjects retain the existing generated URL convention.
- PDF access depends on the BIT Mesra archive being available and the URLs remaining valid.
- Visit/download counting is best-effort and does not block the downloader if the counter service is unavailable.

## License

MIT. See [`LICENSE`](LICENSE).
