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

## Update the Theme Version

The theme version used to build the site is defined in `go.mod` file.

The best practice is to update to released and tested versions. To update to a specific version execute the following command in a terminal/commandline (at the root path of your site repo):

```shell
  hugo mod get github.com/chrede88/L1nkr@vX.Y.Z
```
Replace X,Y & Z with the corresponding version numbers. Releases: [here](https://github.com/chrede88/L1nkr/releases).
Please check if any breaking changes are listed under the release you want to update to, before proceeding.



