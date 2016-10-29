---
layout: post
title: "How to configure Chalk"
description: "Learn more about the config file for Chalk and how to set it up properly."
tags: [web, jekyll]
---

The _config.yml file is the most Important

{% highlight yml %}
# Important settings (change at own risk)

assets:
  compress:
    css: true
    js: true
  features:
    automatic_img_size: false
  sources:
    - _assets/fonts
    - _assets/images
    - _assets/javascripts
    - _assets/stylesheets
    - _vendor/
collections:
  my_tags:
    output: true
    permalink: /tag/:slug/
defaults:
  -
    scope:
      path: ""
      type: my_tags
    values:
      layout: articles_by_tag
exclude:
  - .bowerrc
  - .travis.yml
  - bin/*
  - bower.json
  - circle.yml
  - Gemfile
  - Gemfile.lock
  - README.md
  - vendor/
gems:
  - jekyll-assets
  - jekyll-paginate
  - jekyll-sitemap
permalink: posts/:slug

# Mandatory settings (these are required)

baseurl: /
name: Chalk
paginate: 25
paginate_path: "/posts/page/:num/"
url: http://chalk.nielsenramon.com # add site url http://example.com/
blog_theme: light # Or use dark

# Optional settings

discus_identifier: # Add your Disqus identifier
ga_analytics: # Add your GA Tracking Id
rss_enabled: true # Change to false if not
social:
  dribbble: # Add your Dribbble link
  facebook: # Add your Facebook link
  github: # Add your GitHub link
  linkedin: # Add your LinkedIn link
  twitter: # Add your Twitter handle

{% endhighlight %}