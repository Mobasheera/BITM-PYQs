<div align="center">

<img src="bitlogo.png" alt="BIT Mesra logo" width="180">

# BITM-PYQs — Previous Year Question Papers

**Find your subject. Access your papers. Prepare smarter.**

A lightweight, browser-based question paper finder for BIT Mesra students. Search or select a subject and open the available previous-year question paper links from one place.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwindcss&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=202124)
![Static Website](https://img.shields.io/badge/Website-Static-4A5568?style=flat-square&logo=githubpages&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-34A853?style=flat-square)

[**Open Repository**](https://github.com/Mobasheera/BITM-PYQs) · [**Report an Issue**](https://github.com/Mobasheera/BITM-PYQs/issues)

</div>

---

## 📌 Overview

**BITM-PYQs** is a simple, static web application that brings subject-wise previous-year question paper links together in a single interface. Instead of navigating through long lists or manually locating a subject, students can search by subject code or name, select the required subject, and open its configured paper links.

The project is built with plain HTML, Tailwind CSS (loaded through its CDN), and JavaScript. It does not require a backend server, database, API key, or build process.

> **Note:** The website provides links to question papers hosted by BIT Mesra. It does not host or reproduce the PDF files itself.

## ✨ Features

- **Subject search** — quickly filter subjects by their code or name.
- **Subject selector** — choose a subject from the available subject list.
- **Open all configured papers** — initiate opening the configured paper links for the selected subject with one click.
- **Paper activity list** — view the paper links and the status of each opening attempt.
- **Direct PDF links** — access the original question paper URLs hosted by BIT Mesra.
- **EC257 paper collection** — includes the supplied Spring 2020, Spring 2022, and Spring 2023 papers from the `archive.bitmesra.ac.in` host.
- **Responsive interface** — usable on desktop and mobile screen sizes.
- **Lightweight setup** — runs directly in a modern web browser without installing dependencies.

## 🧰 Technology Stack

| Technology | Role in the project |
|---|---|
| **HTML5** | Page structure, labels, controls, and content |
| **Tailwind CSS** | Utility-based styling and responsive layout, loaded from CDN |
| **JavaScript** | Subject filtering, paper-link generation, and opening paper links |
| **Browser APIs** | Opening paper links in new tabs/windows |
| **GitHub** | Source-code hosting and version control |

## 🧠 How It Works

```text
          Open BITM-PYQs
                │
                ▼
       Search or select a subject
                │
                ▼
       Click "Download all PDFs"
                │
                ▼
       Get configured paper links
                │
                ▼
       Open each paper link
                │
                ▼
       Display paper activity list
                │
                ▼
       View or download PDFs
       from the BIT Mesra archive
```

### Understanding the paper activity list

- **Link listed:** The corresponding paper URL is displayed so it can be opened manually.
- **Opened / request initiated:** The page has attempted to open the paper link in a new tab or window.
- **Popup blocked:** The browser prevented the new tab/window from opening; use the displayed link directly.

The activity list reports opening attempts. It cannot confirm that a PDF was completely downloaded.

## 🚀 Quick Start

### Requirements

- A modern web browser (Firefox, Microsoft Edge, Chrome, or another Chromium/Firefox-based browser).
- Internet connection to load Tailwind CSS from its CDN and access the BIT Mesra PDF archive.

### 1. Clone the repository

```bash
git clone https://github.com/Mobasheera/BITM-PYQs.git
```

### 2. Open the project folder

```bash
cd BITM-PYQs
```

### 3. Launch the website

Open `index.html` directly in your browser.

Alternatively, use the VS Code **Live Server** extension and select **Open with Live Server** on `index.html`.

There is no package installation or compilation step.

## 📚 Available Subjects

The subject selector currently includes the following configured entries:

| Subject Code | Subject Name |
|---|---|
| MA107 | Mathematics-II |
| PH113 | Physics |
| BE101 | Biological Science for Engineers |
| CS101 | Programming for Problem Solving |
| EE101 | Basic of Electrical Engineering |
| EC257 | Electromagnetic Fields and Waves |

The list reflects the subjects currently present in the website's HTML. Paper availability depends on the URLs configured for each subject.

## 📄 EC257 — Electromagnetic Fields and Waves

The following four original archive links are configured for EC257:

| Session | Examination | PDF |
|---|---|---|
| Spring 2023 | End Semester | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2023%20QP/EC257%20ELECTROMAGNETIC%20FIELDS%20AND%20WAVES%20(END_SP23).pdf) |
| Spring 2023 | Mid Semester | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2023%20QP/EC257%20ELECTROMAGNETIC%20FIELD%20AND%20WAVES%20(MID_SP23).pdf) |
| Spring 2022 | End Semester | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2022%20QP/EC257%20ELECTROMAGNETIC%20FIELDS%20AND%20WAVES%20(END_SP22).pdf) |
| Spring 2020 | Mid Semester | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2020%20QP/EC257%20ELECTROMAGNETIC%20FIELDS%20%26%20WAVES%20(MID_SP20).pdf) |

These links intentionally use the `archive.bitmesra.ac.in` hostname and the exact filenames supplied for the project.

## 🗂️ Project Structure

```text
BITM-PYQs/
├── index.html      # Main website, subject list, styling, and JavaScript logic
├── bitlogo.png     # BIT Mesra logo used in the website and README
├── README.md       # Project documentation
└── LICENSE         # MIT License
```

## 🌐 Deployment

BITM-PYQs is a static website and can be deployed using any static hosting service, including **GitHub Pages**.

### Deploy with GitHub Pages

1. Push the project files to your GitHub repository.
2. Open the repository's **Settings** page.
3. Navigate to **Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select the `main` branch and `/ (root)` folder, then save.
6. Open the published URL shown in the GitHub Pages settings.

No server-side runtime is required.

## ⚠️ Browser Notes & Limitations

- **Multiple tabs may be blocked:** Browsers can restrict several tabs or windows opened from one click. Allow pop-ups for the deployed website when prompted, or open the listed paper links individually.
- **Download behavior is controlled by the browser and archive server:** A PDF may open in the browser or download, depending on browser settings and the server's response headers.
- **No completion verification:** A static page cannot reliably verify that a cross-origin PDF has finished downloading. The activity list therefore shows opening attempts, not confirmed downloads.
- **External availability:** PDF links depend on the BIT Mesra archive remaining online and the files remaining available at their original URLs.
- **Internet required:** Tailwind CSS is loaded from a CDN, and question papers are served from external archive URLs.

## 🛠️ Troubleshooting

<details>
<summary><strong>The website opens without styling</strong></summary>

Check your internet connection. Tailwind CSS is loaded from its CDN, so the page needs internet access to load the styles.
</details>

<details>
<summary><strong>Only some PDFs open after clicking the download button</strong></summary>

Your browser may have blocked multiple pop-ups. Allow pop-ups for the website and try again, or use the individual links shown in the paper activity list.
</details>

<details>
<summary><strong>A PDF opens in a tab instead of downloading</strong></summary>

This behavior is determined by the browser's PDF settings and the archive server's response. Use the browser's PDF viewer download control to save the file when it opens in a tab.
</details>

<details>
<summary><strong>A PDF link does not work</strong></summary>

Check that you are connected to the internet and try opening the link directly. The file may have been moved or removed from the BIT Mesra archive.
</details>

## 🤝 Contributions

Suggestions, corrections to paper links, and improvements are welcome. Please open an [issue](https://github.com/Mobasheera/BITM-PYQs/issues) to report a problem or propose an enhancement.

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<div align="center">

**BITM-PYQs**  
*Previous Year Question Papers — BIT Mesra*

Made to make academic resources easier to find and access.

</div>
