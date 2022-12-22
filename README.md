# Baseet - Hugo theme

Baseet is a minimal and clean theme for hugo with a markdown-ish UI.
Baseet means minimal in Arabic.

Forked from [Archie Theme](https://github.com/athul/archie)

## Demo

[Check the Demo](https://blog.ghamza.dev) hosted on GitHub Pages.

## Feature

- Google Analytics
- Callouts
- Tags
- Auto Dark Mode (based on system theme)
- Dark/Light Mode toggle
- tl:dr; frontamatter
- Cache busting for CSS files
- Comment with giscus

## Installation

In your Hugo website directory, create a new folder named theme and clone the repo

```bash
mkdir themes
cd themes
git clone https://github.com/Ghamza-Jd/baseet.git
```

Edit the `config.toml` file with `theme="baseet"`
For more information read the official [setup guide](https://gohugo.io/overview/installing/) of Hugo.

## Writing Posts

Create a new `.md` file in the _content/posts_ folder

```yml
---
title: Title of the post
description:
date:
tldr: (optional)
draft: true/false (optional)
tags: [tag names] (optional)
---
```

## Docs

### Meta

| Name      | Descritpion                                                                  | Possible Values  and Example |
| --------- | ---------------------------------------------------------------------------- | ---------------------------- |
| baseURL   | The website's base url                                                       | `https://my.john.doe`        |
| language  | The website's language to help the page for indexing                         | `en-us`                      |
| title     | Blog's title - its going to appear at the top of the index page              | `John Doe Blog`              |
| theme     | The theme you're using                                                       | `ghamza-archie`              |
| copyright | a copy right message that is going to be displayed at the end of the website | `© John Doe`                 |

Example:

```toml
baseURL = "https://blog.ghamza.dev"
language = "en-us"
title = "Ghamza Blog"
theme = "baseet"
copyright = "© Hamza Jadid"
```

### Params

| Name         | Description                                                                            | Possible Values and Example |
| ------------ | -------------------------------------------------------------------------------------- | --------------------------- |
| mode         | Theme mode                                                                             | `light`, `dark`, or `auto`  |
| useCDN       | A flag to indecate if you want to get the font and icons from a CDN                    | `true` or `false`           |
| subtitle     | A small description that is going to appear right under the website's title            | `An awesome blogger`        |
| support_text | If you have a support message and you want to display it accross your blog put it here | `Support Ukraine 🇺🇦`         |
| gtag_key     | If you want to add google analytics, add your gtag key in this field                   | `G-ABCD12345`               |

Example:

```toml
[params]
mode = "auto"
useCDN = true
subtitle = "Personal blog to share computer science and software engineering articles."
support_text = "🕊️🇵🇸 I stand with humanity, I stand with Palestine 🇵🇸🕊️"
gtag_key = "G-ABCD1234"
```

#### Giscus

[Giscus](https://giscus.app/) can make us add comments to our websites using Github's discussion.

Giscus is defined inside the Params.

We'll nothing to think about here, all you need to do is go to the [Giscus Web App](https://giscus.app/), fill in the form and then come back and replace the values.

Replacement:
| Theme Config      | Values from Giscus     | Comment                                                                          |
| ----------------- | ---------------------- | -------------------------------------------------------------------------------- |
| enabled           | -                      | This is a flag for the template to conditionally add Giscus, defaults to `false` |
| repo              | data-repo              | -                                                                                |
| repo_id           | data-repo-id           | -                                                                                |
| category_id       | data-category-id       | -                                                                                |
| mapping           | data-mapping           | -                                                                                |
| reactions_enabled | data-reactions-enabled | -                                                                                |
| emit_metadata     | data-emit-metadata     | -                                                                                |
| input_position    | data-input-position    | -                                                                                |
| theme             | data-theme             | -                                                                                |
| loading           | data-loading           | -                                                                                |
| lang              | data-lang              | -                                                                                |
| crossorigin       | crossorigin            | -                                                                                |

Example:

```toml
[params.giscus]
enabled = true
repo = "username/repo"
repo_id = "R_repo_id"
category_id = "DIC_category_id"
mapping = "url"
reactions_enabled = 1
emit_metadata = 1
input_position = "top"
theme = "preferred_color_scheme"
loading = "lazy"
lang = "en"
crossorigin = "anonymous"
```

### Favicon

Favicon are defined inside the Params.
You can add some of those fields, I like to put all of them just to see green checks in lighthouse.

| Name             | Description                      | Possible Values and Example |
| ---------------- | -------------------------------- | --------------------------- |
| apple_touch_icon | For iOS and Android devices      |                             |
| s32              | Size for taskbar shortcutFavicon |                             |
| s16              | Size for browser Favicon         |                             |
| manifest         | For extensions                   |                             |

Example:

```toml
[params.favicon]
apple_touch_icon = "https://static.ghamza.dev/icons/apple-touch-icon.png"
s32 = "https://static.ghamza.dev/icons/favicon-32x32.png"
s16 = "https://static.ghamza.dev/icons/favicon-16x16.png"
manifest = "https://static.ghamza.dev/icons/site.webmanifest"
```

### Social

Social are dfined inside the Params.
It's an array of `social` object than contains `name`, `icon` and `url`

Example:

```toml
[[params.social]]
name = "GitHub"
icon = "github"
url = "https://github.com/Ghamza-Jd"

[[params.social]]
name = "rss"
icon = "rss"
url = "https://blog.ghamza.dev/index.xml"
```

## Menu

The menu contains a `main` which is an array that contains a `name`, `url` and a `weight`.

Example:

```toml
[[menu.main]]
name = "Archives"
url = "/posts"
weight = 1

[[menu.main]]
name = "Tags"
url = "/tags"
weight = 2
```

---

## Credits

Forked from [Archie Theme](https://github.com/athul/archie) and Licensed under MIT License
Inspired by design of blog.jse.li
