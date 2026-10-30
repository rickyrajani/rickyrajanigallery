# Ricky Rajani Gallery

The website for rickyrajanigallery.com. It is a single static page with no build step, so GitHub Pages can serve it as-is.

## What's in this folder

```
index.html            the whole site (About, Worlds, The Story of Sitara, Contact)
CNAME                 tells GitHub Pages to answer on rickyrajanigallery.com
.nojekyll             tells GitHub to serve the files untouched
assets/img/           web-sized paintings, the About portrait, and the glass texture
assets/fonts/         the Signarita Zhai wordmark font
assets/favicon.svg    the gold star browser-tab icon
```

## Publish on GitHub Pages

1. Create a new public repository on GitHub, for example `rickyrajanigallery`.
2. Upload everything in this folder to the repository root (drag the files into "Add file → Upload files"). Make sure `CNAME` and `.nojekyll` come along; on a Mac, press Cmd+Shift+. in Finder to see the dot-file.
3. In the repository, go to **Settings → Pages**. Under "Build and deployment", choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. On the same page, the custom domain should already read `rickyrajanigallery.com` (from the CNAME file). Once DNS is working, tick **Enforce HTTPS**.

## Point the Namecheap domain at GitHub

In Namecheap, open **Domain List → Manage → Advanced DNS** for rickyrajanigallery.com. Delete the default parking records, then add:

| Type         | Host | Value                         |
|--------------|------|-------------------------------|
| A Record     | @    | 185.199.108.153               |
| A Record     | @    | 185.199.109.153               |
| A Record     | @    | 185.199.110.153               |
| A Record     | @    | 185.199.111.153               |
| CNAME Record | www  | YOUR-GITHUB-USERNAME.github.io. |

DNS can take from a few minutes to a few hours. GitHub's Pages settings page shows a green check when the domain is verified.

## The wordmark font

"Ricky Rajani Gallery", the "Ricky" sign-off and the large "Sitara" use Signarita Zhai, cut down to only the letters the site needs (`assets/fonts/SignaritaZhai.woff`, 7 KB).

**Licence:** the font's readme says it is free for personal use only. If the site starts selling work, email the author (Rimando "Dondon" Nillo Jr., dondonnillo@gmail.com) for commercial permission, or switch to a script with an open licence such as Mrs Saint Delafield or Herr Von Muellerhoff on Google Fonts.

## The Story of Sitara

Only the title page and dedication are published. Turning the page after the dedication shows a "coming soon" page that invites readers to join the Collectors List. The rest of the story and Plates I–IV are kept off the site, and out of this repository, until launch.

## The Collectors List

The Collectors page (`#collectors`) and the bottom of the Worlds page embed the Substack signup form from rickyrajanigallery.substack.com.

## The stained glass

The book's windows, moon medallion, chapter ornaments and calla lilies are drawn in code (search `windowSVGs`, `medallion`, `lunette` and `calla` in `index.html`), so they stay sharp at any size. Each chapter's glass colours live in `THEMES`. `assets/img/glass.jpg` is the hammered-glass texture laid over them.

## Editing content

- **Contact links** are in the `CONFIG` block near the top of the `<script>` in `index.html`.
- **Paintings** are listed in `PAINT`. To add a new image, resize it to about 1200px on the long side, save as JPEG around 80% quality, and put it in `assets/img/`.

## About image protection

The paintings are published at screen size only (about 1200px), which is too small for a good print. Right-click saving and dragging are switched off as a light deterrent, but anything shown in a browser can still be screenshotted. Keep the full-resolution scans off the site.
