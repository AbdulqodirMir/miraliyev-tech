# miraliyev.tech

Static one-file portfolio, hosted on GitHub Pages with the custom domain miraliyev.tech.

## Structure

- `index.html` - the whole site (master copy, serves `/`)
- `en/index.html`, `ru/index.html`, `uz/index.html` - **exact copies** of the master.
  The site's own script reads the URL path first (`/en`, `/ru`, `/uz`) and forces that
  UI language; the root URL keeps the automatic detection (path -> ?lang= -> browser
  languages -> timezone -> en). There is no language switcher button by design.

## Updating the site (e.g. new portfolio file)

1. Replace `index.html` with the new file.
2. Copy the same file over `en/index.html`, `ru/index.html` and `uz/index.html`
   (all four must stay identical).
3. Commit to `main`. Pages redeploys in about a minute. No DNS changes needed.

DNS lives at manage.get.tech: 4 apex A records to GitHub Pages IPs and a
`www` CNAME to abdulqodirmir.github.io. HTTPS is enforced.
