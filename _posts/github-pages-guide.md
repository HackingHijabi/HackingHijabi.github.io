---
title: "Step-by-Step: Launching Your GitHub Portfolio Site with the Chirpy Jekyll Theme"
author: HackingHijabi
categories: [Article]
tags: [portfolio, chirpy, jekyll, GitHub]
render_with_liquid: false
media_subpath: /images/articles/
image:
	path: mygithub.webp
---

# Create a GitHub Pages Site: yourusername.github.io (Chirpy Theme for Jekyll)
If you've been trying to create a GitHub page for walkthroughs, CTF or whatever interest of yours, this is a simplified way to go about it.

## Prerequisites

Make sure you have:

- A **GitHub account**  
  [How to create one](https://docs.github.com/en/get-started/start-your-journey/creating-an-account-on-github)

- **Git installed locally**  
  [Install Git on Kali Linux](https://www.geeksforgeeks.org/linux-unix/how-to-install-git-on-kali-linux/)

- **Ruby + Bundler installed** (optional for local development)  
  [Install Ruby & Bundler](https://www.geeksforgeeks.org/how-to-install-ruby-bundler-on-linux/)

---

## Step 1: Use the Chirpy Starter Template

1. Visit: [https://github.com/cotes2020/chirpy-starter](https://github.com/cotes2020/chirpy-starter)
2. Click the green **“Use this template”** button.
3. Select **“Create a new repository”**.
4. Name it `yourusername.github.io`.
5. Set permissions to **Public**.
6. Click **“Create Repository”**.

---

## Step 2: Clone to Your Local Machine

```bash
git clone https://github.com/yourusername/yourusername.github.io
cd yourusername.github.io
```

---

## Step 3: Personalize the Site

### `_config.yml`

```yaml
theme: jekyll-theme-chirpy
lang: en
timezone: Africa/Lagos
title: HackingHijabi
tagline: A Girl can Hack
description: >-
  A simple CTF walkthrough journey.
url: "https://hackinghijabi.github.io"
github:
  username: HackingHijabi
twitter:
  username: HackingHijabi
social:
  name: HackingHijabi
  #email: example@domain.com
  links:
    - https://twitter.com/HackingHijabi
    - https://github.com/HackingHijabi
    - https://youtube.com/@hackwithtoibat
theme_mode: dark
avatar: assets/img/toibat.jpg
baseurl: ""
```

---

### `_data/contact.yml`

```yaml
- type: github
  icon: "fab fa-github"

- type: twitter
  icon: "fa-brands fa-x-twitter"

# - type: email
#   icon: "fas fa-envelope"
#   noblank: true

# - type: rss
#   icon: "fas fa-rss"
#   noblank: true
```

> 💡 Comment out unused contact types by adding `#` in front.

---

### `_data/share.yml`

```yaml
platforms:
  - type: Twitter
    icon: "fa-brands fa-square-x-twitter"
    link: "https://twitter.com/intent/tweet?text=TITLE&url=URL"

  - type: Facebook
    icon: "fab fa-facebook-square"
    link: "https://www.facebook.com/sharer/sharer.php?title=TITLE&u=URL"

  - type: Telegram
    icon: "fab fa-telegram"
    link: "https://t.me/share/url?url=URL&text=TITLE"

  # Uncomment if needed:
  # - type: Linkedin
  #   icon: "fab fa-linkedin"
  #   link: "https://www.linkedin.com/feed/?shareActive=true&shareUrl=URL"
  #
  # - type: Weibo
  #   icon: "fab fa-weibo"
  #   link: "https://service.weibo.com/share/share.php?title=TITLE&url=URL"
```

---

## Add Your Avatar

1. Navigate to: `/assets/img`
2. Paste your `.jpg` file (e.g., `toibat.jpg`)
3. Ensure `_config.yml` has:

```yaml
avatar: assets/img/toibat.jpg
```

---

## Create Your Favicons

1. Visit [https://favicon.io/](https://favicon.io/)
2. Upload an image & generate favicons
3. Download the `.zip` file
4. Delete `site.webmanifest` & `browserconfig.xml` (if present)
5. Copy remaining files to `/assets/img/favicons/`  
   *(Create the folder if it doesn't exist)*

---

## Customize the About Page

Open `_tabs/about.md` and edit:

```markdown
---
icon: fas fa-info-circle
order: 4
---

### Hello, HackingHijabi Here.

I will be sharing walkthroughs here to achieve 3 main goals:

* Teach What I Learn  
* Inspire Others — I was inspired by Jaxafed  
* Get Better at Writing
```

---

## Step 4: Commit Your Changes

```bash
git add .
git commit -m "updated template"
git push origin main
```

> 🔐 You’ll be prompted for a **Personal Access Token (PAT)** or **SSH**.

---

## Step 5: Connect to GitHub with SSH

Follow the instructions:  
[Add SSH Key to GitHub](https://www.geeksforgeeks.org/git/how-to-add-ssh-key-to-your-github-account/)

---

## Step 6: Enable GitHub Pages

1. Go to: `https://github.com/yourusername/yourusername.github.io`
2. Open **Settings** > **Pages**
3. Under **Build and Deployment**, set source to **GitHub Actions**
4. You should see:  
   **“Your site is live at https://yourusername.github.io/”**
