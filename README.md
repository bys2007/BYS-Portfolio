# BYS Portfolio

This repository contains the source code for the personal portfolio of **Brillian Yusuf Sejati (BYS)**, hosted on GitHub Pages. The website is specifically designed to showcase skills as a programmer (web developer & IoT) as well as a video editor & visual designer through a modern, interactive, elegant, and fully responsive interface.

## Live Demo
- Production: [https://bys2007.github.io/BYS-Portfolio/](https://bys2007.github.io/BYS-Portfolio/)

## Quick Glance
![BYS Portfolio Screenshot](assets/Screenshot%20(1580).webp)

## Feature Highlights & Page Structure
The site is built with a single-page layout approach that flows smoothly, featuring the following key elements:
- **Bilingual Support (ID/EN)**: The portfolio seamlessly supports both Indonesian and English. The root `index.html` detects browser preferences or saved user settings via `localStorage` and automatically routes visitors to `id.html` or `en.html`. Users can manually toggle the language directly from the navbar.
- **Exclusive Dark Mode Design**: A futuristic visual style featuring a background grid pattern (*bg-grid*), transparent *glassmorphism* panels, and premium typography using the *Space Grotesk* font.
- **Dynamic Hero Background**: The background images in the Hero section change randomly with soft crossfade transitions, drawn dynamically from a manifest file.
- **Smart Navigation (Sticky & Scrollspy)**: A floating navigation header equipped with an active page position detector (*Scrollspy* via `IntersectionObserver`), quick links, and a responsive mobile menu.
- **Two Sides Showcase (I Have Two Sides)**: An interactive toggle feature filtering works between the **Programmer** side (web projects, Laravel systems, Arduino integration) and the **Editor & Designer** side (MV video editing, school cinematography, etc.). The last selected side is saved in the browser's `localStorage`.
- **Journey Timeline**: An educational timeline tracking the growth of BYS's interests from childhood to graduating as one of the top Software Engineering (RPL) students in vocational high school.
- **Dynamic & Deep Zoom Photo Gallery**: Loads documentation asynchronously using a combination of **PhotoSwipe** and **PhotoSwipe Deep Zoom** for a high-resolution lightbox zoom experience without pixelation.
- **Transcripts & Academic Results**: A detailed transcript table from Semester I to the Final Stage Assessment (ASAJ), including internship grades (at PT Telkom Indonesia Regional 4 Semarang) and class rankings.
- **Universal Media Modal**: A one-click pop-up lightbox modal for viewing project images and videos, supporting keyboard navigation (left/right arrows for the mini-gallery and the Escape key).
- **SEO & Performance Optimized**: Fully loaded with Open Graph/Twitter meta tags, `hreflang` tags for internationalization, and lazy-loading logic utilizing `data-src` for embedded YouTube iframes to dramatically reduce initial network requests.
- **Donation & Contact Integrations**: Saweria support link, direct CV download button, and official social media links.

## Technologies Used
- **HTML5**: Semantic elements for clean, SEO-friendly document structures.
- **Tailwind CSS (CDN)**: A utility-first CSS framework for rapid responsive design, custom-configured with extended brand `sky` colors directly in the document head.
- **JavaScript ES6 (Modern Type Module)**: Native interaction logic free from jQuery dependencies, covering asynchronous manifest loading, *Intersection Observer*, modal navigation, language routing, and *localStorage* management.
- **PhotoSwipe & PhotoSwipe Deep Zoom**: Visual libraries for delivering high-quality, interactive photo galleries.
- **Google Fonts (Space Grotesk)**: The primary typography chosen for its clean, modern character.

## Project Structure
```
.
├─ index.html                        # Application entry point and intelligent language router
├─ id.html                           # Indonesian version of the portfolio
├─ en.html                           # English version of the portfolio
├─ README.md                         # Project documentation (this file)
└─ assets/
   ├─ CV — Brillian Yusuf Sejati     # BYS Curriculum Vitae (CV) file
   ├─ Logo bys.webp                  # Site Logo/Favicon
   ├─ Screenshot (1580).webp         # Project screenshot for README
   ├─ icon/                          # Technology & software icons
   │  ├─ programmer/                 # HTML, CSS, JS, PHP, Laravel, React, Arduino, etc.
   │  └─ desainer_editor/            # Alight Motion, Premiere, AE, Blender, Figma, etc.
   ├─ pencapaian/                    # Certificate & award images
   ├─ projek_programmer/             # Project showcase thumbnails/videos
   ├─ random_foto/                   # Collection of photos for the dynamic gallery
   ├─ random_foto_manifest.json      # JSON manifest mapping gallery photo paths
   └─ vendor/                        # Third-party libraries (PhotoSwipe & Deep Zoom)
```

## How to Run Locally
1. Clone or download this repository to your computer.
2. Open the project folder.
3. Run a simple static server to avoid *ES Module* CORS issues and JSON manifest loading constraints. You can use:
   - **Node.js (serve)**:
     ```bash
     npx serve .
     ```
   - **Python**:
     ```bash
     python -m http.server 8000
     ```
   - **VS Code Extension**: Use the **Live Server** feature.
4. Open the provided local address (e.g., `http://localhost:3000` or `http://127.0.0.1:8000`) in your browser.

## Development & Customization
- **Bilingual Contents**: Any content updates must be mirrored in both `id.html` and `en.html` to maintain parity between language versions.
- **Hero & Random Backgrounds**: Edit the `<section id="home">`. To change the randomized hero images, ensure the photos are placed in `assets/random_foto/` and registered within `assets/random_foto_manifest.json`.
- **About & Skills**: Update the profile text and skill tags (`chip`) in `<section id="about">`.
- **Projects**: Add or edit cards inside the `#projectGrid` container. Use the attribute `data-side="dev"` for programming projects and `data-side="edit"` for editing/design projects.
- **Achievements**: Add new certificates formatted as image/video cards in `<section id="achievement">`.
- **Report Card**: Update the grade tables in `<section id="rapor">`.
- **Gallery**: Add new photo files to the `assets/random_foto/` directory and append their new paths into the array inside `assets/random_foto_manifest.json` for automatic discovery by the gallery script.

## Deployment
This site is designed to be entirely static and highly optimized for deployment on:
1. **GitHub Pages** (Automatically active via the `main` branch).
2. **Vercel / Netlify / Cloudflare Pages** by selecting the "Static HTML/No Build" option.

## Contact
Reach out to BYS for collaboration, freelance work, or job opportunities:
- **Email**: [un10102007@gmail.com](mailto:un10102007@gmail.com)
- **GitHub**: [github.com/bys2007](https://github.com/bys2007)
- **Instagram**: [@bys.2007](https://instagram.com/bys.2007/)
- **Location**: Weleri, Kendal, Central Java, Indonesia

Thank you for visiting the BYS Portfolio!
