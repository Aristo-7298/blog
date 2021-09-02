---
title: Second Blog
date: 2021-09-02T07:42:56Z
linktitle: First Blog
weight: 10
---

## Create your Hugo configuration file
Hugo can read your configuration as JSON, YAML or TOML. Hugo supports parameters custom configuration too. Refer to the [Hugo configuration documentation](/overview/configuration/) for details.

![Hugo icon](https://nickopotamus.co.uk/post/hugo-website-rstudio/featured.png)


## Set your configuration publish folder to `_site`
The default is for Jekyll to publish to `_site` and for Hugo to publish to `public`. If, like me, you have [`_site` mapped to a git submodule on the `gh-pages` branch](http://blog.blindgaenger.net/generate_github_pages_in_a_submodule.html), you'll want to do one of two alternatives:

1. Change your submodule to point to map `gh-pages` to public instead of `_site` (recommended).

        git submodule deinit _site
        git rm _site
        git submodule add -b gh-pages git@github.com:your-username/your-repo.git public