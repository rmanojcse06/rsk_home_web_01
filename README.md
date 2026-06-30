# RSK Enterprises Website

Minimal, futuristic single-page website for RSK Enterprises targeting healthcare BDEs in US & Canada.

## 🚀 Deploy to GitHub Pages (Free)

1. Create a new public GitHub repository (e.g. `rsk-enterprises`)
2. Push files:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/rsk-enterprises.git
   git branch -M main
   git push -u origin main
   ```
3. In the repo on GitHub: **Settings → Pages → Source: Deploy from branch → Branch: main → / (root)**
4. Your site will be live at `https://YOUR_USERNAME.github.io/rsk-enterprises` within 2 minutes

## ⚡ Add Cloudflare CDN (Free, Recommended)

1. Sign up at https://cloudflare.com (free plan)
2. Add your domain (or use a free `.pages.dev` subdomain with Cloudflare Pages instead of GitHub Pages)
3. If using a custom domain: point your domain's DNS nameservers to Cloudflare, then set a CNAME record pointing to `YOUR_USERNAME.github.io`
4. Cloudflare handles HTTPS + global CDN automatically

## 📧 Set Up Contact Form (Formspree — Free)

1. Sign up at https://formspree.io (free: 50 submissions/month)
2. Create a new form, select email: `Rajkumarsingaram91@gmail.com`
3. Copy your form endpoint URL (looks like `https://formspree.io/f/xyzabcde`)
4. In `index.html`, find this line:
   ```html
   <form id="contactForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
5. Replace `YOUR_FORM_ID` with your actual form ID

## 💬 Set Up Live Chat (Tawk.to — Free Forever)

1. Sign up at https://www.tawk.to (completely free, no branding)
2. Create a property named "RSK Enterprises"
3. Go to **Administration → Chat Widget → Embed Code**
4. In `index.html`, find the `<!-- REPLACE: Paste Tawk.to script here -->` comment near the bottom
5. Paste the script tag provided by Tawk.to above or below that comment
6. Download the Tawk.to mobile app to get live notifications when BDEs chat

## ✏️ Update Contact Email

Find and replace `Rajkumarsingaram91@gmail.com` in `index.html` — appears in 2 places (contact section + footer).

## 📁 File Structure

```
rsk-enterprises/
├── index.html   ← entire website (HTML + CSS + JS all inline)
└── README.md    ← this file
```
