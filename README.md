# userstyles

UserCSS styles for [Stylus](https://github.com/openstyles/stylus), published on [userstyles.world](https://userstyles.world/user/SignorBananone). All of them use the [Nord](https://www.nordtheme.com/) palette.

Each style lives in its own `.user.css` file. The userstyles.world pages mirror this repository: pushing a new version here, with a higher `@version`, updates the style for everyone who installed it.

## Strava Nord V2

A Nord theme for [Strava](https://www.strava.com/).

- File: [`strava-nord-v2.user.css`](strava-nord-v2.user.css)
- Install: [userstyles.world/style/19531](https://userstyles.world/style/19531) or open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/strava-nord-v2.user.css) with Stylus installed.

The theme lives in a CSS cascade layer, so its `!important` declarations win over Strava's own without specificity tricks. Selectors rely on HTML tags, ARIA roles, `data-testid` attributes and stable class-name prefixes rather than hashed class names, so the theme keeps working across Strava's CSS deploys.

Versions up to 2025.04.30 were a fork of *Strava Darkest Fusion* by ATX (CC BY-SA 4.0). Version 2026.09.30 is a rewrite from scratch and is released under the MIT license.

## Google Scholar Nord

A Nord theme for [Google Scholar](https://scholar.google.com/), including author profiles, metrics, Scholar Labs and the Quick read panel. It applies to every national Scholar domain (`scholar.google.it`, `scholar.google.de`, ...).

- File: [`google-scholar-nord.user.css`](google-scholar-nord.user.css)
- Install: [userstyles.world/style/19493](https://userstyles.world/style/19493) or open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/google-scholar-nord.user.css) with Stylus installed.

## Archlinux Nord

A Nord theme for the Arch Linux websites: [archlinux.org](https://archlinux.org/), the [AUR](https://aur.archlinux.org/), the [wiki](https://wiki.archlinux.org/), the [forums](https://bbs.archlinux.org/), [man pages](https://man.archlinux.org/) and the [security tracker](https://security.archlinux.org/).

- File: [`archlinux-nord.user.css`](archlinux-nord.user.css)
- Install: [userstyles.world/style/19537](https://userstyles.world/style/19537) or open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/archlinux-nord.user.css) with Stylus installed.

Each site has its own section. Stylus' `domain()` also matches subdomains, so the section for archlinux.org itself uses `url-prefix()` to stay off the wiki, forums and other subdomains.

## NextDNS Nord

A Nord theme for the [NextDNS](https://nextdns.io/) dashboard at [my.nextdns.io](https://my.nextdns.io/), including the analytics charts and the logs. The dashboard's light and dark themes both get the same dark Nord colours.

- File: [`nextdns-nord.user.css`](nextdns-nord.user.css)
- Install: [userstyles.world/style/24237](https://userstyles.world/style/24237) or open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/nextdns-nord.user.css) with Stylus installed.

## License

[MIT](LICENSE).
