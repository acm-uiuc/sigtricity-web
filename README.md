---
layout: home
title: Home
nav_exclude: true
permalink: /:path/
seo:
  type: Course
  name: {{ site.title }}
---

# {{site.title}}
This repository is a GitHub Pages template developed for the purpose of quickly deploying SIG websites. In addition to serving plain web pages and files, it provides a boilerplate for:

- [announcements](announcements.md),
- a [calendar](calendar.md),
- a [staff](staff.md) page,
- and a weekly [schedule](schedule.md).

This template that extends the popular [Just the Docs](https://github.com/just-the-docs/just-the-docs) theme, which provides a robust and thoroughly-tested foundation for your website. Just the Docs include features such as:

- automatic [navigation structure](https://just-the-docs.github.io/just-the-docs/docs/navigation-structure/),
- instant, full-text [search](https://just-the-docs.github.io/just-the-docs/docs/search/) and page indexing,
- and a set of [UI components](https://just-the-docs.github.io/just-the-docs/docs/ui-components) and authoring [utilities](https://just-the-docs.github.io/just-the-docs/docs/utilities).

# Recent Announcements

{% assign announcements = site.announcements | reverse %}
{% assign announcement_count = announcements | size %}

<div class="announcements-list">
{% for announcement in announcements limit:5 %}
  {{ announcement }}
{% endfor %}
</div>

{% if announcement_count > 5 %}
  <a href="/announcements" class="see-all-link">See All Announcements</a>
{% endif %}

## Getting Started

Getting started with the ACM SIG template is simple.

1. Create a [new repository based on the template](https://github.com/acm-uiuc/sig-website-template/generate).
1. Update `_config.yml` and `README.md` with your SIG information. [Be sure to update the url and baseurl](https://mademistakes.com/mastering-jekyll/site-url-baseurl/).
1. Configure a [publishing source for GitHub Pages](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages). Your website is now live!
1. Edit and create `.md` [Markdown files](https://guides.github.com/features/mastering-markdown/) to add more content pages.

### Local development environment

Just the Class requires no special Jekyll plugins and can run on GitHub Pages' standard Jekyll compiler. To setup a local development environment, clone your template repository and follow the GitHub Docs on [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll).

## Attribution
* [Just The Class](https://kevinl.info/just-the-class/)
* [Just The Docs](https://just-the-docs.com/)