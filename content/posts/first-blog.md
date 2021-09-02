---
title: First Blog
date: 2021-09-02T07:35:06Z
weight: 10
linktitle: First Blog
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

2. Or, change the Hugo configuration to use `_site` instead of `public`.

        {
            ..
            "publishdir": "_site",
            ..
        }

## Convert Jekyll templates to Hugo templates
That's the bulk of the work right here. The documentation is your friend. You should refer to [Jekyll's template documentation](http://jekyllrb.com/docs/templates/) if you need to refresh your memory on how you built your blog and [Hugo's template](/layout/templates/) to learn Hugo's way.

As a single reference data point, converting my templates for [heyitsalex.net](http://heyitsalex.net/) took me no more than a few hours.
