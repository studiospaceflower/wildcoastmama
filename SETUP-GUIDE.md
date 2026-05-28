# Wild Coast Mama — Site Setup Guide
# How to get this live on Netlify in under an hour

## What you've got

A complete website with:
- Homepage, blog index, sample post page
- Full Wild Coast Mama brand design (Cormorant Garamond, teal palette, everything)
- Decap CMS — a visual editor at yoursite.com/admin so you can write posts without touching code
- Ready to deploy to Netlify for free

---

## Step 1 — Create a GitHub account (if you don't have one)

Go to github.com and sign up for a free account.
GitHub is where your site files live. Netlify reads from it automatically.

---

## Step 2 — Create a new GitHub repository

1. Click the + icon in GitHub → New repository
2. Name it: wildcoastmama
3. Set it to Public
4. Click Create repository

---

## Step 3 — Upload the site files

1. On the repository page, click "uploading an existing file"
2. Drag ALL the files from the wildcoastmama folder (not the folder itself, the files inside)
3. This includes: index.html, blog.html, post.html, netlify.toml, the css/ folder, admin/ folder, posts/ folder
4. Click Commit changes

---

## Step 4 — Deploy to Netlify

1. Go to netlify.com and log into your existing account
2. Click Add new site → Import an existing project
3. Choose GitHub
4. Select your wildcoastmama repository
5. Build settings: leave everything blank (no build command needed)
6. Click Deploy site

Your site will be live in about 30 seconds at a random URL like brave-rabbit-123.netlify.app

---

## Step 5 — Enable Netlify Identity (for the CMS login)

1. In your Netlify dashboard, go to your new site
2. Click Site settings → Identity
3. Click Enable Identity
4. Scroll to Registration → change to Invite only
5. Click Save

---

## Step 6 — Enable Git Gateway (connects CMS to your files)

1. Still in Identity settings
2. Scroll to Services → Git Gateway
3. Click Enable Git Gateway

---

## Step 7 — Invite yourself as a CMS user

1. In Identity → Users
2. Click Invite users
3. Enter your own email address
4. Check your email and accept the invite — set a password

---

## Step 8 — Connect your domain

1. Buy wildcoastmama.co.uk on Namecheap (~£10/year)
2. In Netlify → Domain settings → Add custom domain
3. Follow Netlify's instructions to point Namecheap DNS to Netlify
4. Netlify automatically adds a free SSL certificate

---

## How to write a new post (once everything is set up)

1. Go to wildcoastmama.co.uk/admin
2. Log in with your email and password
3. Click Blog Posts → New Blog Post
4. Fill in: Title, Date, Category, Strapline, Body text, Tilly's note
5. Upload your photo
6. Click Publish
7. The site updates automatically — post is live within 60 seconds

That's it. No code. No files. Just write and publish.

---

## How Claude helps with posts

When you want a post written, send Claude (in this Wild Coast Mama project):

"POST BRIEF
Which post: [title from the content calendar]
Date: [Tuesday date]
What happened this week:
- [bullet]
- [bullet]
Tilly did: [what she did]
Tone: [funny / honest / emotional / practical]"

Claude writes the full post. You copy it into the CMS body field. Done.

---

## File structure reference

wildcoastmama/
├── index.html          ← Homepage
├── blog.html           ← Blog post list
├── post.html           ← Single post template
├── netlify.toml        ← Netlify config
├── css/
│   └── style.css       ← All brand styles
├── admin/
│   ├── index.html      ← CMS login page
│   └── config.yml      ← CMS field definitions
├── posts/
│   └── 2026-05-19-why-we-chose-van-life.md  ← Sample post
└── images/
    └── uploads/        ← Where CMS uploads your photos
