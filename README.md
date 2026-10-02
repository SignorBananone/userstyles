# userstyles

UserCSS styles for [Stylus](https://github.com/openstyles/stylus), most of them also published on [userstyles.world](https://userstyles.world/user/SignorBananone). All of them use the [Nord](https://www.nordtheme.com/) palette.

Each style lives in its own `.user.css` file. The userstyles.world pages mirror this repository: pushing a new version here, with a higher `@version`, updates the style for everyone who installed it.

## Options

Every style has the same options, set from Stylus (the gear icon next to the style, or *Configure* in the manager). The defaults are the dark Nord look.

- **Apply the theme**: always, or only when the browser or system is in dark mode, or only when it is in light mode. When the condition does not hold, the site keeps its own colours.
- **Palette**, listed from the darkest to the lightest:
  1. *Black*: near-black backgrounds with a hint of Nord blue, for OLED screens and dark rooms;
  2. *Deep*: darker than Nord;
  3. *Nord*: the original Polar Night backgrounds with Snow Storm text, the default;
  4. *Dim*: a little lighter than Nord (nord1 as the page background);
  5. *Slate*: the lightest dark palette, grey-blue, with brighter text and slightly lifted accents;
  6. *Fog*: a grey light palette (nord4 as the page background), the least glare;
  7. *Mist*: a soft light palette, between Fog and Snow;
  8. *Snow*: the original Nord light, Snow Storm backgrounds and Polar Night text;
  9. *Paper*: almost white, for bright rooms;
  - *Colourful dark* and *Colourful light*: bluer backgrounds and more saturated Frost and Aurora accents;
  - *Follow the browser*: one dark and one light palette, picked in **Follow the browser: palette when the browser is dark / light** (Nord and Snow by default);
  - *Custom*: the sixteen colours below.

  In every light palette the accents are darkened until they reach a 4.5:1 contrast on cards.
- **Custom palette type** and **Custom nord0 ... nord15**: used only by the *Custom* palette. Each colour picker is labelled with its role (background, surfaces, borders, text, main accent, red for errors, ...). For a light custom palette, put light colours in nord0 to nord3, dark ones in nord4 to nord6, and set the type to *Light*.

The styles are compiled by Stylus' built-in Less preprocessor. Every colour in them is one of the sixteen palette colours, or a `color-mix()` of them, so a palette recolours the whole style. Shades that are not in Nord (a slightly lighter grey, a tinted background) are written as mixes of their neighbours in the palette and follow whichever palette is selected.

## Strava Nord V2

A Nord theme for [Strava](https://www.strava.com/).

- File: [`strava-nord-v2.user.css`](strava-nord-v2.user.css)
- Install: [userstyles.world/style/19531](https://userstyles.world/style/19531) or open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/strava-nord-v2.user.css) with Stylus installed.

The theme lives in a CSS cascade layer, so its `!important` declarations win over Strava's own without specificity tricks. Selectors rely on HTML tags, ARIA roles, `data-testid` attributes and stable class-name prefixes rather than hashed class names, so the theme keeps working across Strava's CSS deploys.

Versions up to 2025.04.30 were a fork of *Strava Darkest Fusion* by ATX (CC BY-SA 4.0). Version 2026.09.30 is a rewrite from scratch and is released under the MIT license. The *Font* option switches back to Strava's older font.

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

A Nord theme for the [NextDNS](https://nextdns.io/) dashboard at [my.nextdns.io](https://my.nextdns.io/), including the analytics charts and the logs. The dashboard's light and dark themes both get the selected palette.

- File: [`nextdns-nord.user.css`](nextdns-nord.user.css)
- Install: [userstyles.world/style/24237](https://userstyles.world/style/24237) or open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/nextdns-nord.user.css) with Stylus installed.

## ChatGPT Nord

A Nord theme for [ChatGPT](https://chatgpt.com/). ChatGPT's light and dark themes both get the selected palette.

- File: [`chatgpt-nord.user.css`](chatgpt-nord.user.css)
- Install: [userstyles.world/style/22760](https://userstyles.world/style/22760) or open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/chatgpt-nord.user.css) with Stylus installed.

ChatGPT derives its colours from a few palettes of CSS variables (`--gray-*`, `--blue-*`, `--red-*`, ...). The style redefines those palettes rather than individual elements, so it survives most redesigns. The Nord values were generated from the site's own: greys mapped onto Polar Night and Snow Storm by lightness, colours onto the Frost or Aurora colour of the same hue.

## Substack Nord

A Nord theme for [Substack](https://substack.com/): the home feed, chat, profiles and every publication on a `*.substack.com` address. Publications on their own domain are not covered.

- File: [`substack-nord.user.css`](substack-nord.user.css)
- Install: [userstyles.world/style/23674](https://userstyles.world/style/23674) or open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/substack-nord.user.css) with Stylus installed.

Each publication sets its own colour theme (cover colours, accent, contrast steps); the style replaces those too, so every publication looks the same.

## YouTube Nord

A Nord theme for [YouTube](https://www.youtube.com/): home, search, watch page, Shorts, menus and live chat.

Besides the main theme variables, the style maps every other colour variable of YouTube's dark theme onto the palette, including the hashed design tokens (`--t` followed by 16 hex digits). YouTube renames some of those tokens on new releases; stale names are harmless, and the next update of the style picks up the new ones.

- File: [`youtube-nord.user.css`](youtube-nord.user.css)
- Install: [userstyles.world/style/27575](https://userstyles.world/style/27575) or open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/youtube-nord.user.css) with Stylus installed.

## Moontower Nord

A Nord theme for the [Moontower](https://www.moontowermoney.com/) blog and its [public Notion pages](https://notion.moontowermeta.com/). Both are public Notion sites, so the style redefines Notion's colour variables; Notion's light and dark themes both get the selected palette.

- File: [`moontower-nord.user.css`](moontower-nord.user.css)
- Install: [userstyles.world/style/17319](https://userstyles.world/style/17319) or open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/moontower-nord.user.css) with Stylus installed.

Versions up to 20240721 were released under CC BY-SA 4.0. The 2026 rewrite is released under the MIT license.

## Proton Nord

A Nord theme for [Proton](https://proton.me/): the account pages (including the VPN dashboard), Mail, Calendar, Drive, Pass and Lumo.

- File: [`proton-nord.user.css`](proton-nord.user.css)
- Install: open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/proton-nord.user.css) with Stylus installed. Not on userstyles.world yet.

Proton builds every app from one set of theme variables (`--background-norm`, `--text-norm`, `--interaction-norm`, ...), which it writes for the theme picked in its settings. The style replaces them for every Proton theme: the core ones by hand, the product-specific ones from Proton's own dark themes moved to the nearest Nord colour. Logos, the sign-in background and the upgrade buttons are recoloured separately.

## Gmail Nord

A Nord theme for [Gmail](https://mail.google.com/): the message list, open conversations, the compose window, the search box and the navigation. It works over every Gmail theme, including picture themes.

- File: [`gmail-nord.user.css`](gmail-nord.user.css)
- Install: open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/gmail-nord.user.css) with Stylus installed. Not on userstyles.world yet.

Gmail's newer components use Material 3 colour roles (`--gm3-sys-color-*`), which the style maps onto the palette. Everything Gmail still writes as a fixed colour (its default light theme, the picture and dark themes, menus and dialogs) comes from a generated block: each colour declaration of Gmail's own stylesheet, mapped onto the palette by property. Hand-written rules on Gmail's class names refine the main surfaces, and the Gmail wordmark is swapped for Google's white-text version. Gmail's icons are bitmaps, dark for light themes and white for dark ones: a filter flattens either kind and tints it, so the icons match whatever Gmail theme is selected. Message bodies keep the sender's colours on a light sheet, since most HTML emails assume a white background.

## Google Nord

One style for several Google services, with a checkbox per service in the Stylus options:

| Module | Sites |
|---|---|
| Google Account | myaccount, accounts (sign-in), myactivity, passwords, takeout |
| Google Search | www.google.*, except Maps |
| Gmail | mail.google.com (same code as Gmail Nord) |
| Google Drive | drive.google.com |
| Docs, Sheets, Slides, Forms | docs.google.com; the document page itself stays white |
| Google Calendar | calendar.google.com; event colours are kept |
| Google Keep | keep.google.com |
| Gemini | gemini.google.com |
| NotebookLM | notebooklm.google.com, notebook.google.com |
| Google Maps | www.google.*/maps; panels only, the map is unchanged |
| Google Scholar | scholar.google.* (same code as Google Scholar Nord) |
| YouTube | www.youtube.com (same code as YouTube Nord) |

- File: [`google-nord.user.css`](google-nord.user.css)
- Install: open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/google-nord.user.css) with Stylus installed. Not on userstyles.world.

A site must not be themed twice: if Gmail Nord, Google Scholar Nord or YouTube Nord is installed too, disable it or untick the matching module.

Drive, Docs, Calendar and the account pages are themed through their Material 3 colour roles and their own token sets (`--dt-*`, `--cal-sys-color-*`, `--identity-colorscheme-*`). Search, Gemini and NotebookLM have dark themes of their own, whose colour values are mapped onto the palette. Keep and Maps paint fixed colours, so their modules are generated from the sites' stylesheets, like Gmail's.

## Amazon Nord

A Nord theme for the Amazon stores (amazon.it, .com, .de, .fr, .es, .co.uk and the other national stores): home, search, product pages, cart, orders, account and lists.

- File: [`amazon-nord.user.css`](amazon-nord.user.css)
- Install: open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/amazon-nord.user.css) with Stylus installed. Not on userstyles.world yet.

Amazon paints its pages with fixed colours, not theme variables, so most of the style is generated: every colour declaration in Amazon's own stylesheets (home, search, product, cart, orders, deals, best sellers, lists and help pages) is moved to the palette by kind (background, text, border) and colour. Hand-written rules follow for the header, the buttons (which Amazon draws with gradients), inputs, pop-overs and the home page widgets. Product pictures have white backgrounds, so they sit on a light "paper"; Amazon's `multiply` blending, which would darken them on dark cards, is switched off. Only `www.` store pages are matched: AWS, Music, Seller Central and the other services on Amazon subdomains are left alone.

## MangaWorld Nord

A Nord theme for MangaWorld: home, archive and filters, manga pages, the chapter reader and the account pages.

- File: [`mangaworld-nord.user.css`](mangaworld-nord.user.css)
- Install: open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/mangaworld-nord.user.css) with Stylus installed. Not on userstyles.world yet.

MangaWorld is built on Bootstrap 4 with fixed colours, so most of the style is generated: every colour declaration in the site's stylesheets (home, archive, manga, reader and login pages) is moved to the palette by kind and colour, with the site's orange becoming Nord orange. Hand-written rules follow for fields, menus, filled buttons and the logo, whose SVG is used as a mask so the word and the stripes take the palette colours. The reader's own dark mode (the moon button) looks the same as the normal one. The site often moves to a new domain, so any `mangaworld.<domain>` address is matched; the adult sister site is not.

## UniBG eLearning Nord

A Nord theme for the University of Bergamo Moodle at [elearning15.unibg.it](https://elearning15.unibg.it/): the front page, dashboard, course list, course pages, drawers, forms and messages.

- File: [`unibg-elearning-nord.user.css`](unibg-elearning-nord.user.css)
- Install: open the [raw file](https://raw.githubusercontent.com/SignorBananone/userstyles/main/unibg-elearning-nord.user.css) with Stylus installed. Not on userstyles.world yet.

The site runs Moodle 4 with the Academi theme, compiled from Bootstrap 4 with fixed colours and no CSS variables, so the style targets Bootstrap's and Moodle's semantic classes (cards, navbars, buttons, alerts, course index, activity items).

## License

[MIT](LICENSE).
