### Step 1 — Create the GitHub repo

1. Go to [github.com/new](https://github.com/new)
2. Name it exactly: `malikabhinav.github.io`
3. Set it to **Public**
4. Do NOT add a README (we'll push one)
5. Click **Create repository**

### Step 2 — Enable GitHub Pages

1. Go to your new repo → **Settings → Pages**
2. Under **Source**, select **GitHub Actions**
3. Save

### Step 3 — Install Hugo on your machine

**Mac:**
```bash
brew install hugo
```

Verify it worked:
```bash
hugo version
```

### Step 4 — Clone your repo locally

```bash
git clone https://github.com/malikabhinav/malikabhinav.github.io.git
cd malikabhinav.github.io
```

### Step 5 — Congo theme setup 

### Issue w/ git submodule : 

```bash
git submodule add -b stable https://github.com/jpanther/congo.git themes/congo
```

1. Submodule pointed to an old commit - The Congo theme had added functions/warnings.html in a newer version, but your submodule was locked to an older commit that predated that file. Hugo found the theme folder but couldn't find that specific partial. 
2. Updating the submodule didn't work - When we tried git pull inside the submodule, it fetched files locally but GitHub Actions kept pulling the old committed pointer — not your updated files.
3. The GitHub Action kept overriding your fix - The submodules: recursive line in deploy.yml told GitHub Actions to re-fetch the submodule on every build — which kept restoring the broken old version and ignoring anything you fixed locally

### Final Fix
Ditching submodules entirely and committing the actual Congo theme files directly into your repo — downloaded from a specific tagged release (v2.8.1) so we knew exactly what we were getting.

Download a specific Congo release tarball  →  Commit files directly  →  No submodule

```bash
# From inside your repo
rm -rf themes/congo

cd themes
curl -L https://github.com/jpanther/congo/archive/refs/tags/v2.8.1.tar.gz -o congo.tar.gz
tar -xzf congo.tar.gz
mv congo-2.8.1 congo
rm congo.tar.gz
cd ..

git add themes/congo
git commit -m "Update Congo theme"
git push
```

### Step 6 — Copy these portfolio files in

Copy everything from this zip into your cloned repo folder.
Your folder should look like this:

```
malikabhinav.github.io/
├── .github/workflows/deploy.yml
├── config/_default/
│   ├── hugo.toml
│   ├── params.toml
│   ├── languages.en.toml
│   └── menus.en.toml
├── content/
│   ├── _index.md
│   ├── about/index.md
│   └── posts/
│       ├── _index.md
│       └── engineering-management-philosophy/index.md
├── static/img/          ← put your avatar photo here as avatar.jpg
└── README.md
```

### Step 7 — Add your avatar photo

Put a square photo of yourself (at least 400×400px) in:
```
static/img/avatar.jpg
```

### Step 8 — Push everything

```bash
git add .
git commit -m "Initial portfolio setup"
git push origin main
```

### Step 9 — Watch it deploy

Go to your repo → **Actions** tab.
You'll see the deploy workflow running. It takes about 60 seconds.
Once it shows a green checkmark, your site is live at:

**https://malikabhinav.github.io**

---

## Writing a new blog post

Every post is just a markdown file. To add a new one:

1. Create a new folder inside `content/posts/`
2. Add an `index.md` file inside it
3. Copy this front matter template at the top:

```markdown
---
title: "Your Post Title Here"
date: 2024-06-01
description: "A one sentence summary shown in post cards and search results."
tags: ["streaming", "leadership", "ad-tech"]
categories: ["Leadership"]
showTableOfContents: true
showReadingTime: true
---

Your content starts here...
```

4. Write your post in Markdown below the `---`
5. `git add . && git commit -m "Add post: your title" && git push`

The site rebuilds and publishes automatically within 60 seconds.

---

## Embedding a Whimsical diagram

Paste this into any post, replacing the URL:

```html
{{< rawhtml >}}
<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
  <iframe
    src="YOUR_WHIMSICAL_EMBED_URL"
    style="position:absolute;top:0;left:0;width:100%;height:100%;border:none;"
    allowfullscreen>
  </iframe>
</div>
{{< /rawhtml >}}
```

## Embedding a Google Slides deck

```html
{{< rawhtml >}}
<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
  <iframe
    src="YOUR_GOOGLE_SLIDES_EMBED_URL"
    style="position:absolute;top:0;left:0;width:100%;height:100%;border:none;"
    allowfullscreen>
  </iframe>
</div>
{{< /rawhtml >}}
```

Get the embed URL from: Google Slides → File → Share → Publish to web → Embed → Copy

---

## Changing the color scheme

Edit `config/_default/params.toml` and change `colorScheme`:

Options: `congo` · `ocean` · `slate` · `fire` · `avocado` · `rose` · `sapphire`

Currently set to: `ocean`

---

## Changing dark/light mode default

In `config/_default/params.toml`:
```toml
defaultAppearance = "dark"   # or "light"
autoSwitchAppearance = true  # follows system preference