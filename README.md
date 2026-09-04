# Site

Static site. No build step, no dependencies.

## Structure

    index.html              homepage + post list
    about.html               about page
    assets/style.css        all styling, shared
    posts/<slug>.html       one file per article

## Adding a post

1. Copy `posts/cage-got-stronger.html` to `posts/your-slug.html`
2. Replace the `<title>`, `<meta name="description">`, `<h1>`,
   `.standfirst`, `.meta` date, and the article body
3. Add an entry to the `.archive` block in `index.html`:

       <div class="entry">
         <a class="title" href="posts/your-slug.html">Title</a>
         <p class="blurb">One or two sentences.</p>
         <div class="when">Date</div>
       </div>

Newest post goes at the top.

## Deploying

This repo deploys to GitHub Pages automatically via
`.github/workflows/pages.yml` on every push to `main`. Live at
https://ddaso-msi.github.io

Cloudflare Pages is also an option: create a project, drag this
folder into the upload box.
