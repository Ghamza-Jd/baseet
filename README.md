# Baseet - Hugo theme

Baseet is a minimal and clean theme for hugo with a markdown-ish UI.
Baseet means minimal in Arabic.

Forked from [Archie Theme](https://github.com/athul/archie)

## Demo

[Check the Demo](https://blog.ghamza.dev) hosted on GitHub Pages :smile:. You can find the source code to that in the `site` branch of this repository

## Feature

- Google Analytics Script
- Callouts
- Tags
- Auto Dark Mode(based on system theme)
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

## Credits

Forked from [Archie Theme](https://github.com/athul/archie) and Licensed under MIT License
Inspired by design of blog.jse.li

---

## Config of the Demo Site

```json
{
    "baseURL": "https://blog.ghamza.dev",
    "language": "en-us",
    "title": "Ghamza Blog",
    "theme": "ghamza-archie",
    "copyright": "© Hamza Jadid",
    "pygmentsstyle": "monokai",
    "pygmentscodefences": true,
    "pygmentscodefencesguesssyntax": true,
    "paginate": 10,
    "params": {
        "mode": "auto",
        "useCDN": true,
        "subtitle": "Personal blog to share computer science and software engineering articles.",
        "support_text": "🕊️🇵🇸 I stand with humanity, I stand with Palestine 🇵🇸🕊️",
        "gtag_key": "G-M9GYS9Z1XC",
        "giscus": {
            "enabled": true,
            "data": {
                "repo": "ghamza-blog/ghamza-blog.github.io",
                "repo_id": "R_kgDOHMIi9w",
                "category_id": "DIC_kwDOHMIi984COoB4",
                "mapping": "url",
                "reactions_enabled": 1,
                "emit_metadata": 1,
                "input_position": "top",
                "theme": "preferred_color_scheme",
                "loading": "lazy",
                "lang": "en"
            },
            "crossorigin": "anonymous"
        },
        "favicon": {
            "apple_touch_icon": "https://static.ghamza.dev/icons/apple-touch-icon.png",
            "s32": "https://static.ghamza.dev/icons/favicon-32x32.png",
            "s16": "https://static.ghamza.dev/icons/favicon-16x16.png",
            "manifest": "https://static.ghamza.dev/icons/site.webmanifest"
        },
        "social": [
            {
                "name": "GitHub",
                "icon": "github",
                "url": "https://github.com/Ghamza-Jd"
            },
            {
                "name": "Facebook",
                "icon": "facebook",
                "url": "https://www.facebook.com/ghamza.tech"
            },
            {
                "name": "LinkedIn",
                "icon": "linkedin",
                "url": "https://www.linkedin.com/in/hamza-jadid"
            },
            {
                "name": "rss",
                "icon": "rss",
                "url": "https://blog.ghamza.dev/index.xml"
            }
        ]
    },
    "menu": {
        "main": [
            {
                "name": "Archives",
                "url": "/posts",
                "weight": 1
            },
            {
                "name": "Tags",
                "url": "/tags",
                "weight": 2
            }
        ]
    }
}
```

---
