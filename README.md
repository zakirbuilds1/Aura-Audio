# AURA Audio

Static website source prepared for GitHub and Vercel on 8 October 2026.
The files under `dist/` exactly match the audited, published source at commit
`acb80a3b9221ebde1ec168462d2443cd884731b7` (saved version 2).

## Image audit

No Unsplash links, API calls, hotlinked images or attribution references were
found in the original site source. The three PNG files are local, generated
project assets. Their original generation briefs are in `image-prompts.json`.
The supplied website/product references were design inputs; screenshots are
not included in the published website.

There are no remote image, font, stylesheet or script dependencies in the
site-owned source. The W3C URL inside the inline SVG favicon is a namespace,
not a downloaded resource. This was a source audit, not a live-browser network
capture or a review of Git history. File hashes are in `audit-manifest.json`.

## Run locally

From this folder, run:

```sh
python3 -m http.server 8080 --directory dist
```

Then open http://localhost:8080 in your browser. No package installation,
build tool, environment variables or backend service is required.

## Add to GitHub

1. Extract the ZIP. Use this project folder as the repository root.
2. Create a new empty GitHub repository named `aura-audio` with your desired visibility.
3. Push the extracted files, including `dist/`, `vercel.json`, this README and the provenance files.
   Do not upload only the ZIP archive.

If using Git, run these commands from the extracted folder. Replace
`YOUR-GITHUB-REPOSITORY-URL` with the new repository's URL before the remote command:

```sh
git init -b main
git add .
git commit -m "Import AURA Audio website"
git remote add origin YOUR-GITHUB-REPOSITORY-URL
git push -u origin main
```

GitHub authentication must already be set up for these commands.

## Deploy on Vercel

Import this GitHub repository as a separate Vercel project. Keep the repository
root as Root Directory. The included `vercel.json` sets:

| Setting | Value |
| --- | --- |
| Framework Preset | Other (`framework: null`) |
| Build Command | Empty; skip build |
| Output Directory | `dist` |
| Environment variables | None required by this source |

After deployment, check the hero and all product images, mobile navigation,
product selection, dialogs and bag controls. Check cursor movement on photos
and cards. Browser Network should show no Unsplash requests; ignore requests
from your browser extensions. Configure the intended Vercel audience separately;
the current Sites access rules are not part of this export.

## Existing functionality and limits

This is a concept storefront. Product names, prices, descriptions and availability
are sample content. The shopping bag exists only for the current page session.
Payments, order processing, customer accounts and shipping services are not connected.
Hosting this code does not add those services.

Photos are fixed; the existing card hover effects are preserved. No runtime
HTML, CSS, JavaScript or images were changed during export. Optional WebMCP
helpers are feature-detected and do not require a server to browse the site.

The export contains no repository history or Sites hosting configuration.
GitHub upload and Vercel deployment have not been performed for this handoff.

## Official deployment references

- GitHub: https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github
- Vercel build settings: https://vercel.com/docs/builds/configure-a-build
- Vercel configuration: https://vercel.com/docs/project-configuration/vercel-json
- Vercel Git integration: https://vercel.com/docs/git

Documentation checked on 8 October 2026.
