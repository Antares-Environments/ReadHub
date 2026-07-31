# ReadHub 

A local, ephemeral, zero-uncertainty PDF rendering engine built for absolute focus and secure document viewing.

## Overview
ReadHub is a lightweight, web-based PDF viewer designed for privacy and distraction-free reading. It processes documents entirely in-browser using volatile memory intercepts (`URL.createObjectURL`), ensuring that your documents are never uploaded to any server.

## Features

- **Volatile File Interception:** Loads PDFs directly from your local filesystem into browser memory. Files are instantly revoked upon loading a new document, ensuring no persistent local caching.
- **Absolute Focus Mode:** A hardware interrupt bound to the **`[H]`** key instantly strips away all navigation docks, leaving you with a distraction-free, full-screen reading experience.
- **Spatial Observer (Page Tracking):** Utilizes `IntersectionObserver` to dynamically track which page you are currently reading, updating the top tracker and auto-scrolling the side dock to keep your navigation in sync.
- **Kinematic UI:** The top and side navigation docks automatically retreat when you scroll down to maximize screen space, and summon back instantly when you scroll up.
- **Client-Side Rendering:** Powered by `pdf.js` with full text-layer support, allowing you to highlight, select, and copy text just like a native PDF application.

## Getting Started

Since ReadHub is a purely static front-end application, no build steps or servers are required to use it locally.

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Antares-Environments/ReadHub.git
   ```
2. **Open the application:**
   Simply double-click on `index.html` to open it in your modern web browser.
3. **Load a Document:**
   Click **[ Load Document ]** in the top dock to select a local PDF file.

## Controls

| Action | Control | Description |
| :--- | :--- | :--- |
| **Focus Mode** | `[ H ]` key | Toggles the visibility of the UI docks. |
| **Summon Docks** | Scroll Up | Reveals the navigation bars. |
| **Hide Docks** | Scroll Down | Hides the navigation bars to clear the viewport. |
| **Jump to Page** | Sidebar Click | Quickly jump to specific pages using the side dock. |

## Built With

- **HTML5 & Vanilla JavaScript:** No heavy frameworks.
- **[PDF.js](https://mozilla.github.io/pdf.js/):** Mozilla's PDF rendering library (bundled in `/static`).
- **CSS3 / Matrix Styling:** Custom glassmorphism and matrix-inspired UI (`matrix.css`).
