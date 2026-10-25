# Probably Qubits

Source for probablyqubits.com. Plain HTML and CSS, no build step.

Every page is self-contained: its styles and the Bloch sphere script are built
into the file, so any page works on its own, even opened outside this folder.
The trade-off is that a style change (a color, a font size) has to be made in
every page. Use find-and-replace across the folder in your editor
(VS Code: Ctrl/Cmd + Shift + H).

## Folder layout

```
index.html              Homepage
learn/index.html        List of explainers
learn/what-is-a-qubit.html   First explainer (use as the template for new ones)
news/index.html         News posts
work/index.html         Projects and talks
about/index.html        About page
404.html                Page-not-found
assets/                 Put images here (e.g. your photo)
CNAME                   Tells GitHub Pages to serve the custom domain
```

## Preview on your computer

Unzip the whole folder first, then open `index.html` in a browser.
Links between pages work locally because they are relative.
The 404 page only works once the site is online.

## Publish on GitHub Pages (free)

1. Create a GitHub account if you do not have one.
2. Create a new public repository, for example `probablyqubits`.
3. Upload everything in this folder to the repository (Add file > Upload files),
   keeping the folder structure. Commit.
4. In the repository, go to Settings > Pages.
   Under "Build and deployment", set Source to "Deploy from a branch",
   branch `main`, folder `/ (root)`. Save.
5. On the same page, enter `probablyqubits.com` under Custom domain and save.

## Point the domain at GitHub

At the registrar where you bought probablyqubits.com, open the DNS settings and add:

| Type  | Host / Name | Value                     |
|-------|-------------|---------------------------|
| A     | @           | 185.199.108.153           |
| A     | @           | 185.199.109.153           |
| A     | @           | 185.199.110.153           |
| A     | @           | 185.199.111.153           |
| CNAME | www         | YOUR-GITHUB-USERNAME.github.io |

Remove any existing "parking" A records first. DNS can take up to a day to update.
Once GitHub shows the domain as verified, tick "Enforce HTTPS" in Settings > Pages.

Check GitHub's docs ("Managing a custom domain for your GitHub Pages site")
in case these addresses have changed.

## Everyday edits

- **New news post:** in `news/index.html`, copy an `<article>` block to the top of the list and edit it.
  Update the three newest on `index.html` too.
- **New explainer:** copy `learn/what-is-a-qubit.html`, rename it, write the content,
  then turn its "Coming soon" card in `learn/index.html` (and on the homepage) into a link.
  The sphere script is already at the bottom of that file, so a copied page can use it.
- **Photo:** save it as `assets/ken.jpg` and follow the comment in `about/index.html`.

## Before launch

- Replace the sample news items.
- Add your LinkedIn URL (search the files for `href="#"`).
- Set up email for hello@probablyqubits.com (most registrars offer free forwarding), or change the address.
