# 🧠 ZombAI — Interactive Project Explorer

<div align="center">

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-00c853?style=for-the-badge&logo=github&logoColor=white)](https://balram3429.github.io/zombai/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![GitHub API](https://img.shields.io/badge/GitHub%20API-v3-181717?style=for-the-badge&logo=github&logoColor=white)](https://docs.github.com/en/rest)

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Maintained](https://img.shields.io/badge/Maintained-Yes-00c853?style=flat-square)](https://github.com/balram3429)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen.svg?style=flat-square)](https://github.com/balram3429/zombai/pulls)
[![Made with ❤️](https://img.shields.io/badge/Made%20with-%E2%9D%A4%EF%B8%8F-red?style=flat-square)](https://github.com/balram3429)
[![Author](https://img.shields.io/badge/Author-balram3429-blue?style=flat-square&logo=github)](https://github.com/balram3429)

<br/>

> **A Google-inspired static landing page that live-fetches and showcases all ZombAI projects from GitHub.**

<br/>

![ZombAI Banner](https://img.shields.io/badge/%F0%9F%A7%A0_ZombAI-Where_Learning_Meets_Intelligence-00c853?style=for-the-badge)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Live Demo](#-live-demo)
- [Features](#-features)
- [Screenshots](#-screenshots)
- [Tech Stack](#-tech-stack)
- [How It Works](#-how-it-works)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [GitHub API Usage](#-github-api-usage)
- [Customisation](#-customisation)
- [Contributing](#-contributing)
- [Author](#-author)

---

## 🌟 Overview

**ZombAI** is a single-file static website that acts as a beautiful, living portfolio page for all `Zomb`-prefixed GitHub repositories. Inspired by the clean simplicity of the Google Search landing page, it greets visitors with a branded multi-color logo and lets them explore every ZombAI project with a single click — no back-end required.

---

## 🚀 Live Demo

| Environment | URL |
|---|---|
| 🌐 GitHub Pages | `https://balram3429.github.io/zombai/` |
| 📁 Local File | Open `zombai.html` directly in any browser |

> **Zero dependencies** — works completely offline for the landing page. Internet is only needed when fetching live repo data via the GitHub API.

---

## ✨ Features

### 🎨 Landing Page
- **Google-style ZombAI logo** — each letter styled in a distinct brand colour (Z=blue · o=red · m=yellow · b=blue · **AI=green**)
- **Animated dark theme** — glowing grid background with radial pulse effect
- **Welcome badge** — live blinking dot indicator
- **Single-click exploration** — one "Explore Projects" button to fetch everything

### 📦 Project Cards
- **Live GitHub API fetch** — pulls all repos matching `/zomb/i` in real-time
- **Sorted by creation date** — newest projects appear first
- **Rich metadata per card:**
  - Language emoji + colour-coded badge
  - Repository description
  - Stars · Forks · Open Issues
  - Last-updated timestamp (human-readable)
  - Topic tags
- **Highlighted repo names** — the `zomb` prefix is highlighted in brand green

### 🔗 Dual Action Buttons per Card
| Button | Action |
|---|---|
| 🔲 **Explore Repo** | Opens the GitHub repository in a new tab |
| 🌐 **View Result** | Opens the GitHub Pages live demo (`username.github.io/repo-name/`). Disabled gracefully when no Pages site exists. |

### 🦶 Footer
> *"Learning is never so Simple — Powered by ZombAI · @balram3429"*

---

## 🛠 Tech Stack

| Technology | Purpose |
|---|---|
| ![HTML5](https://img.shields.io/badge/-HTML5-E34F26?logo=html5&logoColor=white&style=flat-square) | Structure & semantic markup |
| ![CSS3](https://img.shields.io/badge/-CSS3-1572B6?logo=css3&logoColor=white&style=flat-square) | Styling, animations, responsive grid |
| ![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?logo=javascript&logoColor=black&style=flat-square) | GitHub API fetch, dynamic card rendering |
| ![GitHub API](https://img.shields.io/badge/-GitHub%20REST%20API%20v3-181717?logo=github&logoColor=white&style=flat-square) | Live repository data |
| ![Google Fonts](https://img.shields.io/badge/-Google%20Fonts-4285F4?logo=google&logoColor=white&style=flat-square) | Nunito typeface |

**No frameworks. No build tools. No dependencies.**  
One `.html` file — open and run anywhere.

---

## ⚙️ How It Works

```
User clicks "Explore Projects"
        │
        ▼
GitHub REST API  →  GET /users/balram3429/repos
(paginated, up to 200 repos)
        │
        ▼
Filter repos where name matches /zomb/i
        │
        ▼
Sort by created_at (newest first)
        │
        ▼
Render repo cards with live metadata
+ detect GitHub Pages (has_pages flag)
+ construct live URL: balram3429.github.io/{repo-name}/
```

---

## 📁 Project Structure

```
zombai/
├── zombai.html        # ← Entire application (single self-contained file)
└── README.md          # ← This file
```

Everything — HTML, CSS, and JavaScript — lives in a single file for maximum portability.

---

## 🏁 Getting Started

### Option 1 — Open locally

```bash
# Clone the repo
git clone https://github.com/balram3429/zombai.git

# Open in browser
open zombai.html
# or
start zombai.html        # Windows
xdg-open zombai.html     # Linux
```

### Option 2 — Deploy to GitHub Pages

1. Push `zombai.html` to your repository (rename to `index.html` for root deployment)
2. Go to **Settings → Pages**
3. Set source branch to `main` / `master`
4. Your site will be live at `https://<username>.github.io/<repo>/`

### Option 3 — Any static host

Drop `zombai.html` into any static hosting service:

[![Netlify](https://img.shields.io/badge/Deploy%20to-Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white)](https://www.netlify.com/)
[![Vercel](https://img.shields.io/badge/Deploy%20to-Vercel-000000?style=flat-square&logo=vercel&logoColor=white)](https://vercel.com/)
[![Cloudflare](https://img.shields.io/badge/Deploy%20to-Cloudflare%20Pages-F38020?style=flat-square&logo=cloudflare&logoColor=white)](https://pages.cloudflare.com/)

---

## 🔌 GitHub API Usage

The app uses the **unauthenticated GitHub REST API v3**.

```
GET https://api.github.com/users/balram3429/repos
    ?sort=created
    &direction=desc
    &per_page=50
    &page={n}
```

### Rate Limits

| Mode | Limit |
|---|---|
| Unauthenticated | 60 requests / hour per IP |
| Authenticated (token) | 5,000 requests / hour |

> If you hit rate limits, wait ~60 seconds and try again. For high-traffic deployments, add a GitHub personal access token via a proxy or serverless function.

---

## 🎨 Customisation

| Variable / Setting | Location | Description |
|---|---|---|
| `GITHUB_USER` | `<script>` | Change to any GitHub username |
| `ZOMB_PATTERN` | `<script>` | RegEx to filter repo names |
| Logo colours | `.logo .z / .o / .m / .b / .ai` | CSS colour per letter |
| Brand green | `--z-green` | CSS variable (default `#00c853`) |
| Background grid | `body::before` | Adjust opacity or size |

---

## 🤝 Contributing

Contributions, issues and feature requests are welcome!

1. Fork the repository
2. Create a feature branch — `git checkout -b feat/amazing-feature`
3. Commit your changes — `git commit -m 'Add amazing feature'`
4. Push to the branch — `git push origin feat/amazing-feature`
5. Open a Pull Request

[![GitHub Issues](https://img.shields.io/github/issues/balram3429/zombai?style=flat-square&logo=github)](https://github.com/balram3429/zombai/issues)
[![GitHub Forks](https://img.shields.io/github/forks/balram3429/zombai?style=flat-square&logo=github)](https://github.com/balram3429/zombai/network/members)
[![GitHub Stars](https://img.shields.io/github/stars/balram3429/zombai?style=flat-square&logo=github)](https://github.com/balram3429/zombai/stargazers)

---

## 👤 Author

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-balram3429-181717?style=for-the-badge&logo=github)](https://github.com/balram3429)

**Balram Tiwari** — *eat, code, run — repeat*

📍 Chennai, India

</div>

---

<div align="center">

**⭐ If you found this useful, please star the repo — it means a lot!**

<br/>

*Learning is never so Simple — Powered by **ZombAI***

[![forthebadge](https://img.shields.io/badge/Built%20with-❤️%20&%20JavaScript-F7DF1E?style=for-the-badge)](https://github.com/balram3429)

</div>
