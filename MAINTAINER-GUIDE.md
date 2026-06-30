# RSK Enterprises Website — Maintainer Guide
### For Rajkumar Singaram · Last updated: June 2026

---

## 📁 Your 4 Website Files

| File | When to Use |
|------|-------------|
| `index.html` | **Default** — Professional blue. Use this all year round. |
| `index-diwali.html` | **Diwali season** — Saffron/gold with animated diyas, crackers & string lights |
| `index-christmas.html` | **Christmas & New Year** — Crimson/green with snowflakes, gifts & holly |
| `index-green.html` | **Go Green campaigns** — Emerald green with leaf animations & eco quote |

All 4 files have identical content (services, contact info, stats) — only the colors and festival banner change.

---

## 🚀 How to Switch Themes on GitHub Pages

### Step 1 — On your computer

Rename files to swap the active theme:

**To activate Diwali theme:**
```
Rename: index.html        →  index-default.html
Rename: index-diwali.html →  index.html
```

**To go back to default:**
```
Rename: index.html          →  index-diwali.html
Rename: index-default.html  →  index.html
```

*(Same pattern for Christmas and Green)*

### Step 2 — Push to GitHub
```bash
git add index.html index-default.html
git commit -m "theme: switch to Diwali theme"
git push origin main
```

GitHub Pages updates within **1–2 minutes** automatically.

---

## 📅 Festive Season Calendar (Suggested)

| Festival | Start Swap | End Swap | File |
|----------|-----------|----------|------|
| 🪔 Diwali | ~2 weeks before Diwali | 2 days after | `index-diwali.html` |
| 🎄 Christmas / New Year | Dec 15 | Jan 5 | `index-christmas.html` |
| 🌿 Go Green / Earth Day | Apr 20–22 | Apr 25 | `index-green.html` |

---

## ✏️ How to Update Your Contact Email

Your email appears in **2 places** in every `index*.html` file. Open the file in any text editor (Notepad, VS Code) and search for:
```
Rajkumarsingaram91@gmail.com
```
Replace both occurrences with your new email.

---

## 📧 Set Up Formspree (Contact Form)

The contact form is ready — it just needs your Formspree form ID.

1. Go to **https://formspree.io** → Sign Up (free)
2. Create a new form → enter your email: `Rajkumarsingaram91@gmail.com`
3. Copy the form ID (looks like `xyzabcde`)
4. In **all 4 index files**, find this line:
   ```html
   <form id="contactForm" action="https://formspree.io/f/YOUR_FORM_ID"
   ```
5. Replace `YOUR_FORM_ID` with your actual ID (e.g., `xyzabcde`)
6. Push to GitHub

**Free plan:** 50 form submissions/month — plenty for a BDE lead pipeline.

---

## 💬 Set Up Tawk.to Live Chat

BDEs can chat with you directly from the website. You get **mobile push notifications**.

1. Go to **https://www.tawk.to** → Sign Up (free forever)
2. Create a property → name it "RSK Enterprises"
3. Go to **Administration → Chat Widget → Embed Code**
4. Copy the `<script>` tag they give you
5. In all 4 index files, find this comment near the bottom:
   ```html
   <!-- REPLACE: Paste Tawk.to script here -->
   ```
6. Paste the script tag right below that comment
7. Download the **Tawk.to mobile app** → you'll get live push notifications when a BDE chats

---

## 🌐 Deploy to GitHub Pages (First Time)

1. Create a **free GitHub account** at https://github.com
2. Create a **new public repository** (e.g., `rsk-enterprises`)
3. Upload your files (drag-and-drop in GitHub's web UI, or use git):
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/rsk-enterprises.git
   git branch -M main
   git push -u origin main
   ```
4. Go to repository → **Settings → Pages → Source: Deploy from branch → Branch: main → / (root)**
5. Your site will be live at: `https://YOUR_USERNAME.github.io/rsk-enterprises`

---

## ⚡ Add Cloudflare CDN (Optional but Recommended)

Makes your site load faster for US & Canada visitors, and adds free HTTPS.

1. Sign up at **https://cloudflare.com** (free plan)
2. If you have a custom domain (e.g., `rskenterprises.com`):
   - Add your domain to Cloudflare
   - Point your domain's nameservers to Cloudflare
   - Add a CNAME record: `@` → `YOUR_USERNAME.github.io`
3. Cloudflare handles HTTPS, caching, and global CDN automatically

---

## 🔧 Quick Reference — File Structure

```
rsk-enterprises/
├── index.html             ← ACTIVE file (what visitors see)
├── index-diwali.html      ← Diwali theme (swap in for the season)
├── index-christmas.html   ← Christmas theme
├── index-green.html       ← Go Green theme
├── README.md              ← Technical deploy guide
└── MAINTAINER-GUIDE.md   ← This guide (for you!)
```

---

## 📞 Need Help?

If you need to make any changes to the website content (new services, updated stats, testimonials), just let your developer know. All content is in the HTML file — no CMS or database needed.

**Key items to update in the future:**
- ✏️ Replace placeholder testimonials (J. Mitchell, S. Anderson, R. Patel) with real client quotes
- 📊 Update stats (98% accuracy, 24hr response, etc.) as your track record grows
- 🏢 Add your company registration / HIPAA certification details if obtained
- 🔗 Add LinkedIn profile link to footer

---

*Built with ❤️ — Single-file architecture, no subscriptions, no CMS, no maintenance headaches.*
