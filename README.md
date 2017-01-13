
# Modifying content

## Adding a post

Create a post in each language in `_i18n/LANG/_posts/YYY-MM-DD-TITLE.md`. Use the following template:

```md
---
layout: post
title: ...
subtitle: ...
quote: "\"...\""
background: images/posts/YYYY-MM-DD-TITLE.jpg
---

...
```

Add the post to the landing page by adding the following to `_data/index.yml`:

```yml
- href:     YYYY/MM/DD/TITLE.html
  img:      images/posts/YYYY-MM-DD-TITLE.png
  title_en: ...
  text_en:  ...
  title_fr: ...
  text_fr:  ...
```

## Adding a page

Add the page to the root-folder of the site (where the file that you are reading is), in `TITLE.md`. This file should have the following content:

```md
---
layout: page
title: titles.TITLE
subtitle: subtitles.TITLE
quote: quotes.TITLE
background: images/banner.jpg
---

{% translate_file TITLE.md %}
```

Add the page for each language to `_i18n/LANG/TITLE.md`. **These files have no header for Jekyll**.

Add the title, subtitle, and quote for each language to the files `_i18n/LANG.yml`. Each of these files has the following layout:

```md
global:
  english: English
  french: Français
pages:
  TITLE: ...
titles:
  TITLE: ...
subtitles:
  TITLE: ...
quotes:
  TITLE: ...
```

## Previewing

Open terminal: 

```bash
cd /data/documents/sharegrow 
jekyll serve 
```
go to browser and type in http://127.0.0.1:4000/ 

to quit press `ctrl-c`

## Commit changes

```bash
cd /data/documents/sharegrow
git add -A   # (only use -A to commit all changes)
```

to view the status use `git status`


# Source

## Theme

The theme is based on the [Spectral theme by HTML5 UP](http://html5up.net/), which is free for personal and commercial use under the [CCA 3.0 license](html5up.net/license).


