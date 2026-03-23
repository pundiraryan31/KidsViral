# KidsViral AI — YouTube Growth Agent

> A fully self-contained, AI-powered YouTube channel management dashboard for **faceless kids content** (age 5–12). Built as a single HTML file — no framework, no backend, no install required.

---

## What This Is

KidsViral AI is a browser-based growth agent that runs your entire YouTube content pipeline from idea to upload in one place. It combines a structured daily workflow, pre-loaded content strategy, and a live Claude AI assistant — all in a dark-themed, production-grade interface.

It was designed for creators running **faceless animated channels** targeting children aged 5–12, but the pipeline and AI assistant work for any kids YouTube niche.

---

## Features

### ⚡ Dashboard
- At-a-glance channel stats (Subscribers, Views, CTR, Retention)
- Today's video summary with genre chips
- Daily pipeline status tracker (4 steps: Ideas → Script → Titles → Upload)
- Optimal upload schedule by day of week (IST timezone, tuned for Indian school kids audience)

### 💡 Ideas Engine
- Generates 5 viral video concepts per session
- Filter by genre (Fantasy, School Life, Mystery, Humor, etc.)
- Filter by emotional hook (Curiosity, Fear, Humor, Friendship, Adventure)
- Choose Series vs Standalone format
- Each idea shows a virality score out of 10
- One-click "Use This Idea" sends concept directly to Script Writer

### ✍️ Script Writer
- Full 6-scene script structure with:
  - 0–5 second hook
  - Scene-by-scene narration + dialogue
  - Sound effect (SFX) cues per scene
  - Character voice tags
  - Cliffhanger ending + subscribe CTA
- Configurable: target length, characters, ending type
- One-click copy to clipboard

### 🎯 Title & Thumbnail
- 3 CTR-optimized title options with a "Best CTR" recommendation
- 2 visual thumbnail concept previews (rendered in-browser)
- Production plan: animation style, tool stack, music & SFX guide
- Click to select your preferred title and thumbnail

### 📤 SEO & Upload
- Pre-written YouTube description (copy-ready)
- 15 keyword tags (click any tag to highlight, add custom tags)
- Animated 7-step upload checklist that runs in sequence
- AI-optimize button for description rewriting

### 📊 Analytics
- Watch time, impressions, likes, comments
- Audience retention curve (visual bar chart)
- CTR by day of week chart
- AI improvement strategy: drop-off points, high-performing themes, next actions

### 🔁 Pipeline
- One-click "Run Full Pipeline" that simulates the full daily workflow
- Real-time pipeline log with timestamps
- Configurable: niche, language (English/Hindi/Hinglish), upload frequency

### 🤖 AI Assistant
- Live chat powered by the **Anthropic Claude API** (`claude-sonnet-4-20250514`)
- System-prompted as a YouTube growth strategist for kids content
- Pre-loaded quick prompts:
  - Shorts script
  - Thumbnail text ideas
  - Pinned comment
  - Series arc planning
- Copy / Clear response

---

## File Structure

```
youtube-agent/
├── index.html    ← entire app (single file, ~1,960 lines)
└── README.md     ← this file
```

Everything — HTML, CSS, JavaScript, content data — lives in `index.html`. There are no dependencies to install, no build step, and no server required.

---

## Quick Start

### Option 1 — Open Locally
Just double-click `index.html`. It opens directly in any modern browser. All features except the live AI Assistant work offline.

### Option 2 — Deploy to Netlify (30 seconds)
1. Go to [netlify.com/drop](https://app.netlify.com/drop)
2. Drag and drop `index.html` onto the page
3. Get a live public URL instantly (e.g. `https://kidsviral-xyz.netlify.app`)

### Option 3 — Deploy to GitHub Pages
```bash
git init
git add index.html README.md
git commit -m "KidsViral AI launch"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/kidsviral-ai.git
git push -u origin main
```
Then go to repo Settings → Pages → Deploy from `main` branch → `/ (root)`.

### Option 4 — Deploy to Vercel
```bash
npx vercel --yes
```
That's it. Vercel auto-detects the HTML file and deploys in under a minute.

---

## Activating the Live AI Assistant

The AI Assistant panel is wired to the Anthropic API. To enable it:

1. Open `index.html` in a text editor
2. Find this line (around line 1880):
   ```javascript
   const response = await fetch('https://api.anthropic.com/v1/messages', {
   ```
3. Add your API key to the headers object:
   ```javascript
   headers: {
     'Content-Type': 'application/json',
     'x-api-key': 'YOUR_ANTHROPIC_API_KEY_HERE',
     'anthropic-version': '2023-06-01'
   },
   ```
4. Save and reload

> ⚠️ **Security note:** Never expose your API key in a public deployment. For public hosting, proxy the API call through a backend function (Netlify Functions, Vercel Edge Functions, or Cloudflare Workers). The key should never be visible in browser source code on a public URL.

---

## Content Strategy Baked In

The app ships with pre-loaded strategy for the **Indian kids YouTube market**:

| Setting | Value | Reason |
|---|---|---|
| Primary upload time | 5:00 PM IST (weekdays) | Kids return from school |
| Weekend upload time | 10:30–11:00 AM IST | Peak screen time |
| Best upload days | Friday, Saturday, Sunday | Highest impressions for kids content |
| Target video length | 5–7 minutes | Optimal for YouTube Kids algorithm |
| Visual cut pace | Every 2–3 seconds | Matches under-10 attention span |
| Series format | 8 episodes | Drives subscribe + binge loop |

### The 5-Point Retention Formula (built into every script)
1. **0–5 sec hook** — question or visual shock that cannot be skipped
2. **Relatable setup** — school, friends, homework (universal kid experience)
3. **Magic/mystery object** — the curiosity driver
4. **Emotional consequence** — stakes that kids actually care about
5. **Cliffhanger** — forces "Subscribe to see what happens"

---

## Recommended Tool Stack

The app references these external tools for full production:

| Step | Tool | Purpose |
|---|---|---|
| Voiceover | [ElevenLabs](https://elevenlabs.io) | Child-friendly AI voices |
| Video editing | [CapCut](https://capcut.com) | Fast cuts, zoom effects, text overlays |
| Scene generation | [Pictory](https://pictory.ai) | Script-to-video automation |
| Thumbnails | [Canva](https://canva.com) | Bold, expressive thumbnail design |
| Image generation | [Midjourney](https://midjourney.com) | Custom character/scene art |
| Upload automation | YouTube Data API v3 | Scheduled uploads via script |
| Workflow automation | [Make](https://make.com) or [Zapier](https://zapier.com) | Connect all tools in a pipeline |

---

## Rollout Strategy (Don't Automate Everything on Day 1)

```
Week 1–2:  Agent writes script → you review (10 min) → tools generate video
Week 3–4:  Add scheduled uploads + SEO auto-fill
Month 2:   Add ElevenLabs API + Pictory API integration
Month 3:   Full automation — agent runs end-to-end daily
```

The biggest mistake new channels make is over-automating before the content is proven. Use the AI for scripts and ideas first. Automate distribution after you know what works.

---

## Series Ideas Pre-Loaded

The Ideas Engine ships with 5 proven concepts:

1. **The Magic Eraser** — erases memories, erases his friend (9.4/10)
2. **Pause Time Watch** — freezes time but breaks (9.1/10)
3. **The Opposite Shadow** — shadow lives its own life (8.8/10)
4. **The Superpower Lunchbox** — 10-minute powers per food (8.6/10)
5. **The 200-Year-Old Librarian** — immortal teacher mystery (9.0/10)

Each is structured as an 8-episode series to maximize subscriber retention and binge-watching.

---

## Customization

### Change the Channel Niche
Edit the `IDEAS_POOL` array in the `<script>` section to replace the pre-loaded ideas with your own genre.

### Change Upload Timezone
Search for `IST` in the HTML and replace schedule times to match your audience's timezone.

### Add More Titles / Thumbnails
In the `#panel-titles` section, duplicate the `.title-option` divs and edit the text.

### Change the AI System Prompt
Find `const systemPrompt = ` in the script section and rewrite it to match your channel's specific niche, tone, or language.

---

## Browser Support

| Browser | Status |
|---|---|
| Chrome 90+ | ✅ Full support |
| Firefox 88+ | ✅ Full support |
| Safari 14+ | ✅ Full support |
| Edge 90+ | ✅ Full support |
| Mobile Chrome/Safari | ✅ Responsive layout |
