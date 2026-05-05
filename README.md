# 🎬 Grittrix Movies

> **Stream any movie or TV show, free. No subscription. No sign up. No credit card.**

[![Live Site](https://img.shields.io/badge/Live-movies.grittrix.com-E8B44E?style=for-the-badge&logo=google-chrome&logoColor=black)](https://movies.grittrix.com)
[![Built by Grittrix](https://img.shields.io/badge/Built%20by-Grittrix%20Technologies-E8B44E?style=for-the-badge)](https://grittrix.com)
[![License](https://img.shields.io/badge/License-MIT-white?style=for-the-badge)](LICENSE)
[![TMDB](https://img.shields.io/badge/Data-TMDB%20API-01B4E4?style=for-the-badge&logo=themoviedatabase&logoColor=white)](https://www.themoviedb.org)

---

![Grittrix Movies Banner](./disan%20logo.png)

---

## 📖 About

**Grittrix Movies** is a free, open-source movie and TV streaming index built and maintained by [Grittrix Technologies](https://grittrix.com) — an AI-first digital agency based in Kampala, Uganda.

The site aggregates metadata from [The Movie Database (TMDB)](https://www.themoviedb.org) and streams content via the [Vidking](https://www.vidking.net) embed player — all within a single, zero-dependency HTML file. No backend. No database. No cost.

Built to give movie lovers across Africa and the world access to premium content without expensive subscriptions, while showcasing what Grittrix builds for clients.

---

## ✨ Features

- 🎥 **Thousands of movies & TV shows** — powered by TMDB, updated daily
- 🔍 **Instant search** — real-time multi-search across movies, TV & actors (press `/` to open)
- 🎬 **In-site playback** — Vidking iframe player, no redirects, no external tabs
- 🌀 **Stream loading overlay** — smooth "Connecting your stream..." UX while player initialises
- 🖼 **Cinematic hero** — auto-rotating featured titles every 6 seconds with crossfade
- 📺 **TV episode controls** — season/episode selectors with prev/next navigation
- 🗂 **7 curated content rows** — Trending, Top Rated, New Releases, TV Shows, Hidden Gems & more
- 🎛 **Genre filter bar** — filter all content by genre in real-time
- 💀 **Skeleton loading** — shimmer placeholders before content arrives
- 📱 **Fully responsive** — mobile-first, works on any screen size
- ⚡ **Zero dependencies** — one HTML file, vanilla JS, no npm, no build tools

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript (ES6+) |
| Movie Data | [TMDB API v3](https://developer.themoviedb.org/docs) (free) |
| Video Player | [Vidking Embed](https://www.vidking.net) (free iframe) |
| Fonts | Google Fonts — Syne, Inter, JetBrains Mono |
| Hosting | Vercel / Netlify (free tier) |
| Backend | None — fully static |

---

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/grittrix/grittrix-movies.git
cd grittrix-movies
```

### 2. Get a free TMDB API key

1. Go to [themoviedb.org](https://www.themoviedb.org/signup) and create a free account
2. Navigate to **Settings → API → Create → Developer**
3. Fill in:
   - App Name: `Grittrix Movies`
   - App URL: `https://movies.grittrix.com`
   - Summary: *Free movie streaming index*
4. Copy your **API Key (v3 auth)**

### 3. Add your API key

Open `index.html` and find this line near the top of the `<script>` block:

```javascript
const TMDB_API_KEY = 'YOUR_TMDB_API_KEY';
```

Replace `YOUR_TMDB_API_KEY` with your actual key.

### 4. Add your logo files

Place these two files in the same folder as `index.html`:

```
grittrix-movies/
├── index.html
├── logo.png          ← Grittrix Technologies logo (top bar)
├── disan logo.png    ← Grittrix Movies logo (nav)
└── README.md
```

### 5. Open in browser

```bash
# Just open the file — no server needed
open index.html
```

Or serve locally:

```bash
npx serve .
# → http://localhost:3000
```

---

## 🌐 Deployment

### Deploy to Vercel (recommended)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy from project folder
vercel

# Set custom domain
# → Go to Vercel dashboard → your project → Domains → Add movies.grittrix.com
```

### Deploy to Netlify

1. Drag and drop your project folder into [app.netlify.com/drop](https://app.netlify.com/drop)
2. Go to **Domain settings → Add custom domain → movies.grittrix.com**

### GitHub Pages

1. Push to GitHub
2. Go to **Settings → Pages → Source: main branch → / (root)**
3. Your site is live at `https://yourusername.github.io/grittrix-movies`

---

## 📁 Project Structure

```
grittrix-movies/
├── index.html          # Entire app — HTML + CSS + JS in one file
├── logo.png            # Grittrix Technologies logo
├── disan logo.png      # Grittrix Movies nav logo
└── README.md
```

---

## 📡 TMDB API Endpoints Used

```
/trending/all/week              → Hero section + Trending row
/movie/popular                  → Popular movies
/movie/top_rated                → Top rated movies
/movie/now_playing              → New releases
/tv/popular                     → Popular TV shows
/tv/top_rated                   → Top rated TV shows
/search/multi?query={q}         → Universal search
/movie/{id}                     → Movie details & runtime
/movie/{id}/credits             → Cast & crew
/movie/{id}/similar             → Similar movies
/tv/{id}                        → TV show + seasons list
/tv/{id}/season/{n}             → Season episode list
/discover/movie?with_genres={}  → Genre filtering
```

---

## ⚙️ Configuration

All configuration lives at the top of the `<script>` block in `index.html`:

```javascript
const TMDB_API_KEY  = 'YOUR_TMDB_API_KEY';       // ← Required
const TMDB_BASE     = 'https://api.themoviedb.org/3';
const IMG_POSTER    = 'https://image.tmdb.org/t/p/w342';
const IMG_BACKDROP  = 'https://image.tmdb.org/t/p/original';
const IMG_FACE      = 'https://image.tmdb.org/t/p/w185';
```

---

## ⚠️ Legal Disclaimer

Grittrix Movies is a **streaming index** — it does not host, upload, store, or distribute any video content.

- All **movie/TV metadata and images** are provided by [The Movie Database (TMDB)](https://www.themoviedb.org). This product uses the TMDB API but is not endorsed or certified by TMDB.
- All **video streams** are provided by third-party embed services ([Vidking](https://www.vidking.net)). Grittrix has no control over the content or availability of these streams.
- This project is operated for **educational and promotional purposes** by Grittrix Technologies.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first.

```bash
# Fork the repo, make your changes, then:
git checkout -b feature/your-feature-name
git commit -m "feat: describe your change"
git push origin feature/your-feature-name
# → Open a Pull Request
```

---

## 📞 Built by Grittrix Technologies

Grittrix is an AI-first digital agency based in **Kampala, Uganda** — building world-class websites, AI agents, chatbots, mobile money integrations, and software for businesses across Africa and beyond.

| Service | Details |
|---|---|
| 🌐 Website | [grittrix.com](https://grittrix.com) |
| 💳 Payments | [pay.grittrix.com](https://pay.grittrix.com) |
| 🎬 Movies | [movies.grittrix.com](https://movies.grittrix.com) |
| 📍 Location | Kampala, Uganda 🇺🇬 |

> *Need a website, AI agent, chatbot, or mobile money integration? [Talk to Grittrix →](https://grittrix.com)*

---

## 📄 License

MIT License — free to use, modify, and distribute with attribution.

---

<p align="center">
  Made with ❤️ by <a href="https://grittrix.com">Grittrix Technologies</a> · Uganda 🇺🇬
</p>
