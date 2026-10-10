# Privacy policies (static site)

Static, self-contained HTML privacy policies for 9 mobile apps by Dereje G., plus a landing page.
This folder is ready to publish (for example with GitHub Pages using the `docs/` folder).

## Structure

```
docs/
  .nojekyll            # empty; stops GitHub Pages from running Jekyll
  index.html           # landing page with relative links to every policy
  whispervault/index.html
  moneytrack/index.html
  pausegate/index.html
  calsnap/index.html
  bloom/index.html
  pomostreak/index.html
  noir-list/index.html
  vibeshelf/index.html
  digestlocal/index.html
```

Each page is plain HTML5 with inline CSS: responsive, light theme with automatic dark mode
(`prefers-color-scheme`), no JavaScript, no external fonts, no trackers.
The policy URL for an app is `<site-root>/<folder>/`, e.g. `https://<user>.github.io/<repo>/calsnap/`.

## Before publishing

**Replace the placeholder `[MY_SUPPORT_EMAIL]` everywhere** (it appears in all 10 HTML files) with the real
support address, for example:

```bash
grep -rl '\[MY_SUPPORT_EMAIL\]' docs | xargs sed -i 's/\[MY_SUPPORT_EMAIL\]/support@example.com/g'
```

(On macOS use `sed -i ''`.) Then check that no placeholder is left: `grep -r 'MY_SUPPORT_EMAIL' docs`.

Policies are dated "Last updated: October 10, 2026" and describe each app's code as audited on that date.
Update the relevant page (and its date) whenever an app adds an SDK, a permission, an account system or network calls.
