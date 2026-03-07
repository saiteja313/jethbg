# JET Harrisburg — jethbg.org

**Jeeyar Educational Trust Harrisburg** — A community website for spiritual growth, cultural preservation, and service.

Built as a static HTML/CSS/JS site, ready for **GitHub Pages** deployment.

---

## 📁 Project Structure

```
jethbg/
├── index.html              ← Homepage
├── css/
│   └── style.css           ← All styles (saffron/gold + maroon theme)
├── js/
│   └── main.js             ← Navigation, lightbox, scroll animations
├── pages/
│   ├── about.html          ← About Us + About Swamiji
│   ├── events.html         ← Upcoming & past events
│   ├── shlokas.html        ← Shloka/prayer PDFs for reading
│   ├── flyers.html         ← Event flyer archive
├── assets/
│   ├── images/             ← Event photos (add your .jpg/.png files here)
│   ├── pdfs/               ← Shloka PDF files (add your .pdf files here)
│   └── flyers/             ← Event flyer images (add your .jpg/.png files here)
└── README.md
```

---

## 🚀 Deploy to GitHub Pages (Step by Step)

### 1. Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click the **+** button → **New repository**
3. Repository name: **`jethbg.org`** (or `jethbg-website`)
4. Set to **Public**
5. **Do NOT** initialize with a README (we already have one)
6. Click **Create repository**

### 2. Push the Code to GitHub

Open your terminal and navigate to the project folder:

```bash
cd jethbg

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial JET Harrisburg website"

# Connect to your GitHub repo (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/jethbg.org.git

# Push
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repo on GitHub: `https://github.com/YOUR_USERNAME/jethbg.org`
2. Click **Settings** (tab at the top)
3. In the left sidebar, click **Pages**
4. Under "Source", select **Deploy from a branch**
5. Branch: **main**, folder: **/ (root)**
6. Click **Save**
7. Wait ~2 minutes, then your site will be live at:
   `https://YOUR_USERNAME.github.io/jethbg.org/`

### 4. Connect Your Custom Domain (jethbg.org)

#### In GitHub:
1. Go to **Settings → Pages**
2. Under "Custom domain", type: **`jethbg.org`**
3. Click **Save**
4. Check **Enforce HTTPS**

#### In Your Domain Registrar (GoDaddy, Namecheap, Google Domains, etc.):

Add these **DNS records**:

| Type  | Name | Value                       |
|-------|------|-----------------------------|
| A     | @    | 185.199.108.153             |
| A     | @    | 185.199.109.153             |
| A     | @    | 185.199.110.153             |
| A     | @    | 185.199.111.153             |
| CNAME | www  | YOUR_USERNAME.github.io     |

DNS changes may take up to 24–48 hours to propagate.

---

## 📝 How to Update Content

### Add Event Photos
1. Place image files in `assets/images/`
   ```html
   <img src="../assets/images/your-photo.jpg" alt="Event Description">
   ```
3. Commit and push to GitHub

### Add Shloka PDFs
1. Place PDF files in `assets/pdfs/`
2. In `pages/shlokas.html`, update the `href` attribute:
   ```html
   <a href="../assets/pdfs/your-shloka.pdf" target="_blank" class="shloka-btn">📄 Open PDF</a>
   ```
3. Commit and push to GitHub

### Add Event Flyers
1. Place flyer images in `assets/flyers/`
2. In `pages/flyers.html`, replace placeholder with:
   ```html
   <img src="../assets/flyers/your-flyer.jpg" alt="Event Name" class="flyer-image">
   ```
3. Commit and push to GitHub

### Add New Events
Edit `pages/events.html` and copy an existing card block, updating the details.

### Update Contact Form
The form currently uses a JavaScript demo handler. For real submissions, sign up for a free **Formspree** account:
1. Go to [formspree.io](https://formspree.io) and create a form
2. Add `action="https://formspree.io/f/YOUR_FORM_ID"` and `method="POST"` to the `<form>` tag
3. Remove the JavaScript form handler from `js/main.js`

---

## 🎨 Customization

### Logo
Replace the `JH` text logo with your actual logo:
1. Place your logo image in `assets/images/logo.png`
2. In all HTML files, replace the `.logo-icon` div with:
   ```html
   <img src="assets/images/logo.png" alt="JET HBG" style="width:52px;height:52px;border-radius:50%;">
   ```
   (Use `../assets/images/logo.png` for files in the `pages/` folder)

### Colors
Edit the CSS variables at the top of `css/style.css` to change the theme colors.

### Social Media Links
Find all `footer-social` sections and update the `href` attributes with your actual social media URLs.

---

## 🔗 Useful Links

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Formspree (free form backend)](https://formspree.io)
- [Chinna Jeeyar Swamiji](https://chinnajeeyar.org/)
- [JET USA](https://jetusa.org)
- [JET UK](https://jetuk.org)

---

© 2026 Jeeyar Educational Trust Harrisburg. All rights reserved.
