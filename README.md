# Jeevan Jayasuriya — Personal Academic Website

A clean, professional multi-page academic portfolio website built with HTML, CSS, and vanilla JavaScript. Designed to be hosted on **GitHub Pages**.

---

## 📁 File Structure

```
jeevanrj.github.io/
│
├── index.html          ← Homepage
├── research.html       ← Research page
├── publications.html   ← Publications page
├── teaching.html       ← Teaching & Mentorship page
├── activities.html     ← Activities page
├── blog.html           ← Blog page
├── cv.html             ← CV page
│
├── css/
│   └── style.css       ← Shared styles for all pages
│
├── js/
│   └── main.js         ← Shared JavaScript (nav, active link)
│
├── images/             ← Put your photos/images here
│   └── profile2.jpg    ← Your profile photo (already linked from GitHub)
│
└── files/
    └── Jeevan_Jayasuriya_Resume.pdf   ← Your CV PDF
```

---

## 🚀 How to Deploy on GitHub Pages

### Option A — Upload via GitHub website (easiest)

1. Go to **github.com** and open your repository: `JeevanRJ/jeevanrj.github.io`
2. Delete all existing files (or keep your `images/` and `files/` folders)
3. Click **"Add file" → "Upload files"**
4. Upload the following:
   - All `.html` files (index, research, publications, teaching, activities, blog, cv)
   - The `css/` folder with `style.css` inside
   - The `js/` folder with `main.js` inside
5. Click **"Commit changes"**
6. Your site will be live at `https://jeevanrj.github.io` within ~1 minute ✅

### Option B — Git command line

```bash
# Clone your repo
git clone https://github.com/JeevanRJ/jeevanrj.github.io.git
cd jeevanrj.github.io

# Copy all the new files into this folder
# (replace existing index.html, add new html files, css/, js/ folders)

# Push to GitHub
git add .
git commit -m "New multi-page academic website"
git push origin main
```

---

## ✏️ How to Edit Your Content

Search for `Replace with` or `Add` in any HTML file — those are your placeholders.

### index.html (Homepage)
- Your bio text is in the `<p>` tag under the hero section
- Social links are the `<a>` tags with `✉ Email`, `Google Scholar`, etc.

### research.html
- Edit the research area cards (titles + descriptions)
- Update the "Current Project" section with your actual project

### publications.html
- Copy/paste a `<div class="pub-card">` block for each publication
- Set `data-type="journal"` or `data-type="conf"` for filtering to work
- Add real DOI links

### teaching.html
- Fill in course names, terms, and student names in mentorship

### activities.html
- Replace timeline items with your real presentations, service, awards

### blog.html
- Each blog card links to `href="#"` — change this to the actual HTML file for each post
- Create `blog-post-1.html`, `blog-post-2.html` etc. for individual posts

### cv.html
- Fill in the CV rows with your real education, experience, and publications
- The PDF download button already points to your existing PDF

---

## 🎨 Customisation

All colors are defined as CSS variables at the top of `css/style.css`:

```css
:root {
  --navy:    #0f1b35;   /* Main dark color */
  --accent:  #2563a8;   /* Blue accent */
  --gold:    #c8922a;   /* Gold accent */
}
```

Change these to restyle the entire site at once.

---

## 📱 Mobile Support

The site is fully responsive. On small screens, the navigation links collapse into a hamburger menu (☰) that the user can tap to open.

---

## 💡 Adding Blog Posts

For each blog post, create a new file like `blog-post-neuroergonomics.html`.
Copy this starter template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Post Title — Jeevan Jayasuriya</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
<nav>
  <!-- copy nav from any other page -->
</nav>
<div class="page">
  <div class="section">
    <div class="container-sm">
      <p class="section-label">Research</p>
      <h1 style="font-family:'DM Serif Display',serif; font-size:2rem; color:var(--navy); margin-bottom:0.5rem;">Your Post Title</h1>
      <p style="color:var(--text-muted); font-size:0.85rem; margin-bottom:2rem;">April 2025 · 5 min read</p>
      <div style="line-height:1.9; color:var(--text-mid);">
        <p>Your post content here...</p>
      </div>
    </div>
  </div>
</div>
<footer><!-- copy footer from any other page --></footer>
<script src="js/main.js"></script>
</body>
</html>
```

Then in `blog.html`, update the card's `href="#"` to `href="blog-post-neuroergonomics.html"`.

---

Built with ❤️ for Jeevan Jayasuriya · jeevanrj.github.io
