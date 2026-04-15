# admatthews.co.uk 

**Adam Matthews - Personal HyperFollow / LinkTree style landing page.**

Built with [Hugo](https://github.com/gohugoio/hugo) - (Fast and flexible static site generator).

Themed with [L1nkr](https://github.com/chrede88/L1nkr) - (Simple mobile-first LinkTree style Hugo Theme).


![Example screenshot of the home page](./assets/landing-page.jpg)

## Features

- Simple LinkTree theme, designed for mobile-first.
- Automatically dark mode (based on system setttings).
- More than 40 supported brand links.
- Healthcheck endpoint (/healthcheck.json).
- Automated updates (Uses a Github actions to automatically detect and apply dependency updates).


---

## Deployment (Cloudflare Pages)

The site is deployed via [Cloudflare Pages](https://pages.cloudflare.com/), connected directly to this repository. Any push to `main` triggers an automatic rebuild and deploy.

### Annual copyright year rebuild

The footer copyright year is rendered dynamically at build time by Hugo. A GitHub Actions workflow (`.github/workflows/annualRebuild.yaml`) triggers a Cloudflare Pages rebuild on 1st January each year to keep it current.

**One-time setup required:**

1. In your Cloudflare Workers/Pages project, go to **Settings → Builds → Deploy hooks** and create a new hook.
2. Copy the generated webhook URL.
3. In this GitHub repository, go to **Settings → Secrets and variables → Actions** and add a secret named `CLOUDFLARE_DEPLOY_HOOK_URL` with that URL as the value.

The scheduled workflow will then `POST` to that URL each New Year, triggering a fresh build.

---

## Update the Theme Version

The theme version used to build the site is defined in `go.mod` file.

The best practice is to update to released and tested versions. To update to a specific version execute the following command in a terminal/commandline (at the root path of your site repo):

```shell
  hugo mod get github.com/chrede88/L1nkr@vX.Y.Z
```
Replace X,Y & Z with the corresponding version numbers. Releases: [here](https://github.com/chrede88/L1nkr/releases).
Please check if any breaking changes are listed under the release you want to update to, before proceeding.



