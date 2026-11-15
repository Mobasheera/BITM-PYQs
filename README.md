<div align="center">

<img src="bitlogo.png" alt="BIT Mesra logo" width="180">

# BITM-PYQs Downloader

**Your question papers. One click away.**

A lightweight, browser-based question paper downloader for BIT Mesra. Search or select a subject, then send its configured previous-year question paper PDF links directly to your browser's download handling — without opening a separate visible tab for every paper.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=202124)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/Hosted_on-GitHub_Pages-222222?style=flat-square&logo=githubpages&logoColor=white)
![Static Website](https://img.shields.io/badge/Website-Static-34A853?style=flat-square)
![License: MIT](https://img.shields.io/badge/License-MIT-34A853?style=flat-square)

</div>

---

## 📌 Overview

**BITM-PYQs Downloader** is a simple static website that helps students find and download previous-year question papers from **Birla Institute of Technology, Mesra (BIT Mesra)**.

Instead of navigating through multiple archive pages and searching for individual PDFs, users can search for a subject by its code or name, select it, and click **Download all PDFs**. The website submits the configured PDF URLs to the browser and displays the links submitted for that subject.

The project is designed to be hosted directly on **GitHub Pages**. It does not require a backend, database, server, package installation, or local runtime.

## ✨ Features

- **Subject search** — find a subject using its subject code or name.
- **Subject dropdown** — browse and select from the available subjects.
- **Bulk download requests** — submit all configured PDF links for the selected subject with one click.
- **No mass tab opening** — uses hidden browser frames for download requests instead of intentionally opening a visible tab for every paper.
- **Submitted-paper list** — displays the paper links sent to the browser after the download button is clicked.
- **EC257 archive support** — includes the supplied original PDF links hosted on `archive.bitmesra.ac.in`.
- **Lightweight interface** — a responsive interface built with HTML, JavaScript, and Tailwind CSS.
- **GitHub Pages ready** — deploy directly from a repository; no build process is required.

## 🧰 Technology Stack

| Technology | Role in BITM-PYQs |
|---|---|
| **HTML5** | Website structure, subject selector, search field, and download interface |
| **JavaScript** | Subject filtering, PDF URL generation, and browser download requests |
| **Tailwind CSS** | Styling, layout, spacing, and responsive design |
| **GitHub Pages** | Static website hosting |
| **BIT Mesra archive** | Source of the question paper PDF files |

## 🧠 How It Works

```text
           User opens BITM-PYQs
                    │
                    ▼
       Search or select a subject
                    │
                    ▼
           Click "Download all PDFs"
                    │
                    ▼
        Get configured PDF URLs
                    │
                    ▼
       Submit each URL to browser
          using hidden frames
                    │
                    ▼
       Browser handles each request
                    │
                    ▼
       Submitted-paper list appears
```

### What happens after clicking Download?

1. The website identifies the selected subject.
2. It obtains the PDF URLs configured for that subject.
3. It submits each URL to the browser through a hidden iframe-based request.
4. The browser and the remote archive server determine whether each response is downloaded, displayed, or rejected.
5. The page lists the paper links submitted to the browser.

> **Important browser limitation:** The website cannot reliably verify whether a cross-origin PDF exists, is a valid PDF, or has finished downloading. The archive server controls its response headers, and browsers control download behavior. Therefore, the on-page list means **Sent to browser**, not **Successfully downloaded**. The browser may also ask permission to allow multiple downloads.

## 📚 Available Subjects

The current subject selector includes:

| Subject Code | Subject |
|---|---|
| MA107 | Mathematics-II |
| PH113 | Physics |
| BE101 | Biological Science for Engineers |
| CS101 | Programming for Problem Solving |
| EE101 | Basic of Electrical Engineering |
| EC257 | Electromagnetic Fields and Waves |

The subject list and paper URL configuration are maintained in `index.html`.

## 📄 EC257 — Electromagnetic Fields and Waves

The project includes these four supplied EC257 PDF URLs from the official BIT Mesra archive:

| Session | Examination | Archive |
|---|---|---|
| Spring 2023 | End Semester | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2023%20QP/EC257%20ELECTROMAGNETIC%20FIELDS%20AND%20WAVES%20(END_SP23).pdf) |
| Spring 2023 | Mid Semester | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2023%20QP/EC257%20ELECTROMAGNETIC%20FIELD%20AND%20WAVES%20(MID_SP23).pdf) |
| Spring 2022 | End Semester | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2022%20QP/EC257%20ELECTROMAGNETIC%20FIELDS%20AND%20WAVES%20(END_SP22).pdf) |
| Spring 2020 | Mid Semester | [Open PDF](https://archive.bitmesra.ac.in/UploadedDocuments/adminexam/files/SP2020%20QP/EC257%20ELECTROMAGNETIC%20FIELDS%20%26%20WAVES%20(MID_SP20).pdf) |

These links use `archive.bitmesra.ac.in` as supplied.

## 🚀 How to Use

1. Open the BITM-PYQs website.
2. Type a subject code or name into **Search subject**, or choose a subject from the dropdown.
3. Click **Download all PDFs**.
4. The website submits the configured PDF links to your browser.
5. Check the browser's Downloads panel for the files and the **Sent to browser** section on the page for the submitted paper links.

If the browser blocks multiple automatic downloads, allow multiple downloads for the website in your browser's site settings and click the download button again.

## 🌐 Deploy on GitHub Pages

BITM-PYQs is a static website and can be hosted directly using GitHub Pages.

### Requirements

- A GitHub account
- A GitHub repository
- `index.html`, `bitlogo.png`, and `LICENSE`

### 1. Upload the project files

Keep the website files in the repository root:

```text
BITM-PYQs/
├── index.html
├── bitlogo.png
├── README.md
└── LICENSE
```

### 2. Push the files to GitHub

Commit and push the project files to your repository's publishing branch.

### 3. Enable GitHub Pages

1. Open your repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select the required branch (for example, `main`) and the root folder (`/`).
5. Click **Save**.

### 4. Visit the published website

Once GitHub Pages finishes deploying, open the Pages URL shown in **Settings → Pages**.

There is no build command, dependency installation, or server configuration.

## 🗂️ Project Structure

```text
BITM-PYQs/
├── index.html   # Complete website, subject list, URL generation, and download logic
├── bitlogo.png  # BIT Mesra logo and website favicon
├── README.md    # Project documentation
└── LICENSE      # MIT License
```

## 🔒 Browser Compatibility & Limitations

- The website does not intentionally open a visible tab for every PDF request.
- The browser may block multiple automatic downloads until the user grants permission.
- Cross-origin PDF downloads are controlled by the remote archive server and the browser.
- The HTML `download` attribute is only a hint and is not guaranteed to force a download from another domain.
- A static GitHub Pages website cannot reliably inspect remote PDF responses unless the remote server allows the required cross-origin access.
- The **Sent to browser** list records submitted links; it does not confirm successful or completed downloads.
- Generated URLs for subjects other than EC257 follow the URL pattern implemented in `index.html`. A generated link may not correspond to an existing paper on the archive.

## 🛠️ Troubleshooting

<details>
<summary><strong>Only some PDFs are downloaded</strong></summary>

The archive server may not have every generated paper URL, or it may respond in a way that causes the browser to display or reject the file. Check the browser's Downloads panel and the individual archive URL.
</details>

<details>
<summary><strong>The browser blocks multiple downloads</strong></summary>

Open the browser's site permissions for your BITM-PYQs website and allow multiple automatic downloads. Return to the website and click **Download all PDFs** again.
</details>

<details>
<summary><strong>The PDF opens instead of downloading</strong></summary>

The remote archive server controls the response headers. If it serves the PDF for inline viewing instead of as an attachment, the browser may display it rather than save it automatically. A static website cannot override that server-side behavior reliably.
</details>

<details>
<summary><strong>Subject search does not show a result</strong></summary>

Clear the search field or check the subject code/name. The search filters the subjects currently present in the dropdown; it does not search the entire BIT Mesra archive.
</details>

## 🛣️ Possible Future Enhancements

- Add more subjects and verified question paper links.
- Add additional archive sessions as they become available.
- Provide clearer per-paper request feedback.
- Add an optional manually maintained catalogue of confirmed PDF links.

## 📄 License

This project is distributed under the [MIT License](LICENSE).

---

<div align="center">

**BITM-PYQs Downloader**

*Your question papers. One click away.*

Made to make accessing BIT Mesra previous-year question papers simpler.

</div>
