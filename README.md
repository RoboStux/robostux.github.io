<p align="center">
  <img src="https://global.media.robo.st/logo.png" width="300" alt="RoboStux">
</p>

# robostux.github.io

The GitHub Pages site for the [RoboStux](https://github.com/RoboStux) organisation. Anyone who visits
`https://robostux.github.io` is sent straight on to the organisation's page,
[github.com/RoboStux](https://github.com/RoboStux). RoboStux's own website is [robo.st](https://robo.st).

## How it works

`index.html` is a single static page with a meta refresh (and a canonical link) pointing at
`https://github.com/RoboStux`, so the redirect happens as soon as the page loads, with no JavaScript.
`.github/workflows/pages.yml` publishes it to GitHub Pages, so the repository's **Settings → Pages → Source**
must be **GitHub Actions**.

To change where it sends people, edit these two lines in `index.html`:

```html
<meta http-equiv="refresh" content="0;url=https://github.com/RoboStux" />
<link rel="canonical" href="https://github.com/RoboStux" />
```

## Testing

```bash
bash tests/version.sh
```

Then open `index.html` in a browser and check that it lands on github.com/RoboStux.

## Versioning

This project uses [Date Versioning](https://datevers.ing): each release is numbered by its UTC release date as `YY.MM.DD` (for example `26.10.23`), with `-1`, `-2`… for later releases the same day. See [CHANGELOG.md](CHANGELOG.md) for what changed in each release.

Releases are made on the `test` branch and go live when its pull request into `main` is merged; see [CONTRIBUTING.md](CONTRIBUTING.md#branches).

## License

(C) StuxieDev.

---

*Written & Maintained by <img src="https://global.media.stuxie.dev/icon.png" height="14" alt="StuxieDev" valign="middle"> [StuxieDev](https://stuxie.dev).*

*[A StuxieDev Project](https://projects.stuxie.dev)*
