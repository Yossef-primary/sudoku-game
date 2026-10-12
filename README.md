# Sudoku Master 🧩

A modern, responsive, web-based Sudoku game built with vanilla HTML5, CSS3, and JavaScript. Zero dependencies, zero build steps, and 100% client-side.

---

## ✨ Features

- **Dynamic Puzzle Generator**: Generates unique, playable Sudoku puzzles on the fly with 4 difficulty levels: *Easy*, *Medium*, *Hard*, and *Expert*.
- **Intuitive UI & Controls**:
  - Clean visual design with 3x3 subgrid demarcation.
  - Interactive highlighting (row, column, 3x3 block, and matching numbers).
  - Dark Mode & Light Mode support (persisted across sessions).
  - Responsive layout optimized for desktop, tablets, and smartphones.
- **Assistance & Gameplay Tools**:
  - **Pencil / Notes Mode**: Toggle pencil marks to note down candidate digits. Auto-clears notes when a valid digit is placed.
  - **Undo**: Step back previous moves and notes (supports `Ctrl+Z` / `Cmd+Z`).
  - **Erase**: Clear any player-entered digit or note (`Backspace` or `Delete`).
  - **Hint**: Instantly reveal the solution for the selected cell.
  - **Check Solution**: Real-time validation of entered numbers.
  - **Remaining Counts**: Virtual number pad displays how many of each digit (1–9) remain to be placed.
  - **Mistake Counter & Timer**: Track your solving time and errors with pause/resume support.
  - **Confetti Victory Modal**: Celebrate your win with stats and a replay button.

---

## 🚀 How to Run Locally

Because this game is completely self-contained in a single file (`index.html`), running it is effortless:

1. Double-click [index.html](file:///Users/ywspswsn/Projects/AgenticProgramming/index.html) to open it directly in any modern web browser (Chrome, Safari, Firefox, Edge).
2. Alternatively, use Python's built-in HTTP server:
   ```bash
   python3 -m http.server 8080
   ```
   Then visit `http://localhost:8080` in your browser.

---

## 🌐 Free Deployment Instructions

You can host and share this project publicly in just a few minutes using any of the following free platforms:

### Option 1: GitHub Pages (Recommended)
1. Initialize a git repository and commit your files:
   ```bash
   git init
   git add .
   git commit -m "Initial commit of Sudoku Master"
   ```
2. Create a new public repository on [GitHub](https://github.com/new) (e.g., `sudoku-game`).
3. Link your remote repository and push:
   ```bash
   git branch -M main
   git remote add origin https://github.com/<your-username>/sudoku-game.git
   git push -u origin main
   ```
4. In your GitHub repository:
   - Go to **Settings** > **Pages** (under the "Code and automation" section).
   - Under **Build and deployment** > **Source**, choose **Deploy from a branch**.
   - Select **Branch**: `main` and folder `/ (root)`.
   - Click **Save**.
5. Within 1–2 minutes, your game will be live at `https://<your-username>.github.io/sudoku-game/`!

---

### Option 2: Netlify Drop (Instant Drag & Drop, No Git Required)
1. Go to [Netlify Drop](https://app.netlify.com/drop).
2. Drag and drop the folder containing `index.html` onto the upload zone.
3. Your game is deployed immediately and you will receive a free public URL (e.g., `https://random-name.netlify.app`).

---

### Option 3: Cloudflare Pages / Vercel
1. Push your repository to GitHub.
2. Sign in to [Cloudflare Pages](https://pages.cloudflare.com/) or [Vercel](https://vercel.com/).
3. Click **Add New Project** and select your GitHub repository.
4. Leave build command empty and root directory as `./`.
5. Click **Deploy** to get a free custom URL and global CDN hosting.
