# A Sunday to Remember – Poster Maker
**Boundless Love Church, Jinja**

A web app that lets anyone personalise the event poster by uploading their own photo into the circle frame, then downloading their customised poster.

---

## 📁 Folder Structure

```
sunday-poster/
│
├── index.html          ← The whole app (HTML + CSS + JS in one file)
│
└── images/
    └── poster.jpg      ← The event poster image (your Avator_Poster-01.jpg)
```

> **That's it.** Two things: one HTML file and the poster image.  
> No frameworks, no build tools, no dependencies to install.

---

## 🖥️ How to Run Locally (Test on Your Computer)

1. Make sure your folder looks exactly like the structure above.
2. Open a terminal in the `sunday-poster` folder and run:
   ```
   npx serve .
   ```
   Or if you have Python installed:
   ```
   python -m http.server 8080
   ```
3. Open your browser and go to `http://localhost:8080`

> ⚠️ **Do NOT just double-click index.html** — it won't work because browsers block local image loading for security. Always use a local server.

---

## 🚀 Deploying to Vercel via GitHub

### Step 1 – Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in (or create a free account).
2. Click the **+** button → **New repository**.
3. Name it: `sunday-poster` (or any name you like).
4. Set it to **Public** (required for free Vercel hosting).
5. Click **Create repository**.

### Step 2 – Upload Your Files to GitHub

**Option A – Upload via Browser (easiest):**
1. On your new repo page, click **Add file → Upload files**.
2. Upload `index.html`.
3. Then create the `images/` folder: click **Add file → Create new file**, type `images/poster.jpg` in the name field, but **don't save** — instead go back and use **Upload files** while inside the `images/` folder path.

**Option B – Using Git on your computer (recommended):**
```bash
# Inside your sunday-poster folder:
git init
git add .
git commit -m "Initial poster maker"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/sunday-poster.git
git push -u origin main
```

### Step 3 – Deploy to Vercel

1. Go to [vercel.com](https://vercel.com) and sign in with your GitHub account.
2. Click **Add New → Project**.
3. Find your `sunday-poster` repo and click **Import**.
4. On the configuration screen:
   - **Framework Preset:** `Other`
   - **Root Directory:** `./` (leave default)
   - **Build Command:** *(leave empty)*
   - **Output Directory:** `./` (leave as `.`)
5. Click **Deploy**.
6. Wait ~30 seconds. Vercel gives you a live link like:  
   `https://sunday-poster.vercel.app`

> 🎉 **Your poster maker is now live!** Share the link and anyone can upload their photo and download a customised poster.

---

## 📱 Mobile-Friendly Notes

- The app is fully responsive — works on phones and tablets.
- On mobile, tapping **Choose Photo** opens the camera or photo gallery.
- The layout stacks vertically on small screens.

---

## ✏️ Customising the Circle Position

If the photo circle doesn't align perfectly with the white circle on your poster, open `index.html` and find this section:

```javascript
// ── CIRCLE POSITION ──
const CIRCLE = { cx: 450, cy: 610, r: 118 };
```

Adjust these values:
| Value | Meaning |
|-------|---------|
| `cx`  | Horizontal centre of the circle (left ↔ right) |
| `cy`  | Vertical centre (up ↕ down) |
| `r`   | Radius (size of the circle) |

The canvas is 900×900 pixels. The poster image is scaled to fit this size.

---

## 🔄 Updating the Poster Image

Just replace `images/poster.jpg` with a new image (keep the same filename), then push to GitHub — Vercel will auto-redeploy.

---

## 📞 Support

Boundless Love Church · www.thegoodworddailydevotional.org  
+256 751 575 372 or +256 771 452 654
