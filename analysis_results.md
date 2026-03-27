# Project Analysis: vishalgimhan.github.io

Based on studying the repository at `e:\Projects_Work\vishalgimhan.github.io`, here is the full picture of the site built with this GitHub Pages template.

## Overview
This repository is a Jekyll-powered personal website built upon the **Academic Pages** template (forked initially from *Minimal Mistakes Jekyll Theme*). It is designed to host the academic portfolio, personal blog, publications, talks, and teaching materials of Vishal Gimhan. 

The site is built automatically via GitHub Pages whenever changes are pushed to the relevant branch.

## Key Configuration
The site's main configuration is heavily driven by `_config.yml`. Here are the primary settings for the site:
- **Site Title & Author**: Vishal Gimhan
- **Bio**: "Dedicated and detail-oriented individual with a strong academic background and hands-on experience in various areas of Data Analytics..."
- **URLs and Socials**: Configured with LinkedIn, GitHub (`vishalgimhan`), Instagram (`_vishal.gimhan_`), and Email.
- **Base URL**: Set to `https://vishalgimhan.github.io`
- **Markdown Processor**: `kramdown` (GitHub Flavored Markdown)
- **Theme/Repository Base**: `academicpages/academicpages.github.io`

## Site Structure & Content Collections
Jekyll organizes structured content into "collections". This site uses several specific collections defined in `_config.yml`, each mapping to a top-level directory:

1. **`_pages/`**: Contains the core standalone pages of the site (e.g., Homepage, About, CV, Markdown syntax guide).
2. **`_posts/`**: Used for a standard blog. It currently contains standard Jekyll blog posts if any exist.
3. **`_publications/`**: A collection for research papers, manuscripts, and books. It contains markdown files representing specific publications (e.g., `2024-02-17-paper-title-number-4.md`).
4. **`_talks/`**: A collection for presentations, tutorials, and talks. It contains files like `2014-03-01-talk-3.md`.
5. **`_teaching/`**: A collection for courses or teaching materials.
6. **`_portfolio/`**: A collection for portfolio projects, containing a mix of HTML and Markdown pieces.

## Layouts, Includes, and Styling
- **`_layouts/`**: Contains the HTML structures for different page types (e.g., `single.html`, `talk.html`, `archive.html`). Markdown files inherit these layouts via their frontmatter (e.g., `layout: single`).
- **`_includes/`**: Contains reusable components (e.g., the author profile sidebar, headers, footers, navigation). The `author-profile.html` specifically renders the sidebar using the author settings from `_config.yml`.
- **`_sass/`**: Contains SCSS stylesheets that define the visual theme. These are compiled by Jekyll into CSS. The main style is typically compressed for performance (`style: compressed`).
- **`assets/`** & **`images/`**: Used for static files, CSS outputs, JS, and image assets.
- **`files/`**: Typically used for hosting downloadable files, like PDFs for papers or the site owner's Curriculum Vitae.

## Automation and Scripting
- **`markdown_generator/`**: This directory contains useful internal scripts (Jupyter notebooks and Python scripts) provided by the Academic Pages template. These scripts allow the user to automatically generate markdown files for publications and talks from a TSV (Tab-Separated Values) format, simplifying the process of migrating large CVs.
- **`talkmap/`**: A feature specific to this theme that can generate a visual map of where talks have been given.

## Local Development
As per the `README.md`, the site can be run locally using standard Ruby-based Jekyll commands:
```bash
bundle install
jekyll serve -l -H localhost
```
Alternatively, there is a `Dockerfile` provided, allowing you to run the local server entirely via a Docker container without needing Ruby installed on the host machine.

## Conclusion
This is a comprehensive, statically generated GitHub Pages site. Any new content can simply be added by creating a new markdown file with the correct frontmatter (title, date, layout, etc.) in the respective collection folder (`_posts/`, `_publications/`, etc.), and the site will dynamically rebuild.
