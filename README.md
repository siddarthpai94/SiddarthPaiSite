# siddarthpai.in

Personal website, blog, and video courses — powered by Jekyll + GitHub Pages.

## Quick Start

1. Push this entire folder to a GitHub repo
2. Go to **Settings → Pages → Source: main branch**
3. Set custom domain to `siddarthpai.in`
4. Done — GitHub builds Jekyll automatically

## Adding a Blog Post

Create a new file in `_posts/` with this naming format:

```
_posts/YYYY-MM-DD-your-post-title.md
```

Example: `_posts/2026-03-01-my-new-post.md`

Add this front matter at the top:

```yaml
---
layout: post
title: "Your Post Title"
date: 2026-03-01
category: Engineering    # Engineering, Product, Career, AI, etc.
read_time: "5 min read"
description: "A brief description for SEO and previews."
---

Your content here in Markdown...

## You can use headings

And **bold**, *italic*, [links](https://example.com), code blocks, etc.
```

## Adding a Video Course

Create a new file in `_courses/` with any name:

```
_courses/your-course-name.md
```

Add this front matter:

```yaml
---
layout: course
title: "Your Course Title"
description: "Course description for the listing page."
level: Beginner           # Beginner, Intermediate, Advanced
lessons: 8
duration: "4.5 hours"
video_id: "YOUTUBE_ID"    # Just the ID, not the full URL
# OR for Loom:
# loom_id: "YOUR_LOOM_ID"
modules:
  - title: "Module 1 Title"
    duration: "20 min"
  - title: "Module 2 Title"
    duration: "35 min"
---

Course description and details in Markdown here...
```

### Getting the YouTube video ID
From `https://www.youtube.com/watch?v=abc123xyz` → the ID is `abc123xyz`

### Getting the Loom ID
From `https://www.loom.com/share/abc123xyz` → the ID is `abc123xyz`

## File Structure

```
├── _config.yml          # Site settings
├── _layouts/            # Page templates
│   ├── default.html
│   ├── post.html
│   └── course.html
├── _includes/           # Reusable components
│   ├── head.html
│   ├── nav.html
│   └── footer.html
├── _posts/              # Blog posts (Markdown)
├── _courses/            # Video courses (Markdown)
├── assets/css/
│   └── style.css        # All styles
├── blog/
│   └── index.html       # Blog listing page
├── courses/
│   └── index.html       # Courses listing page
├── index.html           # Homepage
├── CNAME                # Custom domain
└── README.md
```

## DNS Setup (GoDaddy)

Add these A records (don't touch MX records — email stays safe):

| Type  | Name | Value             |
|-------|------|-------------------|
| A     | @    | 185.199.108.153   |
| A     | @    | 185.199.109.153   |
| A     | @    | 185.199.110.153   |
| A     | @    | 185.199.111.153   |
| CNAME | www  | YOUR_USERNAME.github.io |
