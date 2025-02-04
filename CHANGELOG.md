# Changelog

All notable changes to this project (since its fork) are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [2.0.2] - 2023-02-06

### Added

* config option: `footer.useColumns`
  * if set to false, toggle footer style to left-aligned (instead of columns).


### Changed

* exampleSite/config.yaml > `baseURL` changed to localhost:1313.
* If content file for hero-item.html provides no button text, hide button.
* If content file for hero.html provides no image, just show header horizontally centered (and hide button if no text defined).


## [2.0.1] - 2023-01-31

### Added

* Support including website's custom javascript (see README.md)
* Support merging website's custom styling into theme's styling (see README.md)


### Changed

* Moved `static/images` to subfolder exampleSite.


### Removed

* `images/` folder.

 
### Fixed

* Placement of cookie notification: now truly stays at the window's bottom.
* Defined `sameSite` value for cookies (web browser was showing warnings).


## [2.0] - 2023-01-20

### Added

* Localization support
  * in config.yaml: navbar, sidebar, footer.
  * in landing page.
* SEO meta support for
  * OpenGraph
  * Twitter
  * Schema
    * Organization
* Other SEO
  * page param "seo_title"
* Default Archetype
* Image Gallery support
* YouTube Video support
* Website Cookies notification
* Color Palette support to recolor this theme


### Changed

* Landing page site data (previously in config.yaml) is now defined in website's index.md file's front matter (i.e. SITE-variables were changed to PAGE-varibles).
* All URLs are expected to be internal and respect the user's currently selected language; except for cases where external URLs are expected, e.g. for social media.
* Property names are called "name" instead of "title", if they represent e.g. menu options in the navbar exactly that; and not "link", which is the element


### Removed

* Site param `include_footer` from front matter; show footer at all times.
* Flex Card styling (is unused)


### Fixed

* Property names are called "url", if they are exactly that; and not "link", which is the element.
* Accessed wrong site param in navbar-clone for navbar logo: should be height, not width


### Security

* Add `noopener, nofollow` for offsite URLs.


## [1.1] - 2022-12-10

### Added

* Support for copyright notice
* "_markup/render-link": adds *noopener* and *nofollow* relation to markdown links in `content/`, if external link (i.e. URL begins with "http")
* Allow configuring Feature Card height


### Changed

* Condense subtitle{number}.html shortcodes
  * Breaking Change: see exampleSite/content/agb.md
* Condense title{number}.html shortcodes
  * Breaking Change: see exampleSite/content/agb.md


## [1.0] - 2022-12-08

> Basically a cleanup of hugo-fresh while preserving functionality


### Added

* exampleSite: added gohugo privacy settings to config.yml


### Changed

* Upgrade fontawesome to 6.2.1-web
* Upgrade bulma to 0.9.4
* Update jQuery to 3.6.1
* Default page background color is dark (defines footer color), sections overwrite to white/grey
* Replace hard-coded section color with "every nth-child"-logic


### Removed

* jquery.panelslider (unused)
* feather-icons (replaced by fontawesome icons)
* google font "Open Sans" (also removes google api)


### Fixed

* Images in sections not shown in some browsers (previously, it was only working for card icons)
* If javascript was disabled, preloader animation was playing indefinitely
