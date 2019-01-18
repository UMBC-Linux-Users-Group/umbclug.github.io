# ritlug.github.io

[![CircleCI](https://circleci.com/gh/RITlug/ritlug.github.io.svg?style=svg&circle-token=b80b9ee3852aa0b52f578b434c6224971fc73d97)](https://circleci.com/gh/RITlug/ritlug.github.io)
[![Code Climate](https://codeclimate.com/github/RITlug/ritlug.github.io/badges/gpa.svg)](https://codeclimate.com/github/RITlug/ritlug.github.io)
[![Issue Count](https://codeclimate.com/github/RITlug/ritlug.github.io/badges/issue_count.svg)](https://codeclimate.com/github/RITlug/ritlug.github.io)

> RITlug's current website.

## Table of Contents
* [About](#about)
* [Adding Content](#adding-content)
* [Updating meeting times / places](#updating-meeting-times--places)

## About

The website's last major update was Summer 2018, but content dates back to 2015.

The site is built using [Jekyll](https://jekyllrb.com/), [Bootstrap](https://getbootstrap.com/) (via CDN), [Font Awesome](https://fontawesome.com/) (via CDN), & [GitHub Pages](https://help.github.com/categories/github-pages-basics/).
[PDF.js](https://mozilla.github.io/pdf.js/) is used for embedding PDFs in pages (via CDN).
"Pretty links" is turned on in the Jekyll configuration.
The `github-pages` Gem is used to simplify dependencies.
The live site is updated by committing changes to the `master` branch.
_The site uses an undocumented feature of Jekyll where categories are defined using `category/_posts/` instead of `_posts/category/`._

## Adding Content

Add a new `.md` file to one of the `_posts/` folders for a category.
Assets should be stored in a folder within that category, for example, `talks/slides/` or `projects/assets/`.
Asset file names should have enough info in the file name to know what references it (such as the associated talk date for slides) or be in a subfolder for things with a lot of assets (such as the TigerOS project).

Current categories:
* ~Announcements (`announcements/`)~ (deprecated)
* Events (`events/`)
* Meetings & Meetups (`meetings-meetups/`) (note that these pages aren't linked from anywhere other than feeds, they are more for the metadata)
* Projects (`projects/`)
* Talks (`talks/`)

Please see [this runbook page](http://runbook.ritlug.com/infrastructure/website/) for more info.

## Updating meeting times / places

Edit `_config.yml` and update the settings "ritlug-time", "ritlug-place", and
"ritlug-day".
These are used (and should be used) everywhere on the website
the meeting time and place are referenced so that they can be updated in
one place.
Please note that this does NOT update events in the iCal feed.
