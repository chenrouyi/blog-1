# Type on Strap 

[![Build Status](https://travis-ci.org/sylhare/Type-on-Strap.svg?branch=master)](https://travis-ci.org/sylhare/Type-on-Strap)
[![Gem Version](https://badge.fury.io/rb/type-on-strap.svg)](https://badge.fury.io/rb/type-on-strap)

A free and open-source [Jekyll](https://jekyllrb.com) theme. Based on Rohan Chandra [type-theme](https://github.com/rohanchandra/type-theme) with a few new features:

* Responsive design
* Portfolio page for your projects
* Tags compatibility
* Bootstrap : [Get Bootstrap](http://getbootstrap.com/)
* Search feature : [Simple-Jekyll-Search](https://github.com/christian-fei/Simple-Jekyll-Search)
* Math Rendering : [KateX](https://github.com/Khan/KaTeX)
* Nice fonts : [Font Awesome](https://fontawesome.com/), [Source Sans Pro](https://fonts.google.com/specimen/Source+Sans+Pro), [Pacifico](https://fonts.google.com/specimen/Pacifico?selection.family=Pacifico) 
* Seo Tags : [Jekyll-seo-tag](https://github.com/jekyll/jekyll-seo-tag)
* Syntax Highlighting: Easily customisable [Base16](https://github.com/chriskempson/base16)
* Free of rights images from [pexels](https://www.pexels.com/)

> [Demo Site](https://sylhare.github.io/Type-on-Strap/)
 
[![Default Type on Strap blog](https://github.com/Sylhare/Type-on-Strap/blob/master/screenshot.png?raw=true)](https://sylhare.github.io/Type-on-Strap/)

## Table of Contents

1. [Usage](https://github.com/Sylhare/Type-on-Strap#Usage)
2. [Structure](https://github.com/Sylhare/Type-on-Strap#structure)
3. [Configure Type on Strap](https://github.com/Sylhare/Type-on-Strap#configure-type-on-strap)
4. [Other Layouts](https://github.com/Sylhare/Type-on-Strap#other-layouts)
5. [Feature pages](https://github.com/Sylhare/Type-on-Strap#feature-pages)
6. [Advanced](https://github.com/Sylhare/Type-on-Strap#advanced)
7. [License](https://github.com/Sylhare/Type-on-Strap#license)

## Usage

### As a ruby gem

Check out this tutorial: [Use as Ruby Gem](https://github.com/Sylhare/Type-on-Strap#use-as-ruby-gem)

### As a github page

1. Fork and clone the [Type on Strap repo](https://github.com/sylhare/Type-On-Strap): `git clone https://github.com/Sylhare/Type-on-Strap.git`
2. Install [Jekyll](https://jekyllrb.com/docs/installation/): `gem install jekyll`, check [#1](https://github.com/Sylhare/Type-on-Strap/issues/1) if you have a problem.
3. Install the theme's dependencies: `bundle install`
4. Customize the theme
	- Github Page: [update `_config.yml`](https://github.com/Sylhare/Type-on-Strap#site-configuration)
5. Run the Jekyll server: `bundle exec jekyll serve`

## Structure

Here are the main files of the template

```bash
jekyll-theme-basically-basic
├── _includes	               # theme includes
├── _layouts                   # theme layouts (see below for details)
├── _portfolio	               # collection of article to be populated in the portfolio page
├── _posts                     # Blog posts
├── _sass                      # Sass partials 
├── assets
|  ├── js	               # theme javascript, Katex, jquery, bootstrap, jekyll search, 
|  ├── css                     # isolated Bootstrap, font-awesome, katex and main css
|  ├── fonts		       # Font-Awesome, and other fonts
|  └── img		       # Images used for the template
├── pages
|   ├── 404.md		       # To be displayed when url is wrong
|   ├── about.md               # About example page
|   ├── gallery.md             # Gallery page for your photos
|   ├── portfolio.md	       # Portfolio page for your projects
|   ├── search.html	       # Search page
|   └── tags.md                # The tag page
├── _config.yml                # sample configuration
└── index.html                 # sample home page (blog page paginated)
```
	
## Configure Type on Strap

Open `_config.yml` in a text editor to change most of the blog's settings.

If a variable in this document is marked as "optional", disable the feature by removing all text from the variable. 


### Site configuration
Configure Jekyll as your own blog or with a subpath in in `_config.yml`:

Jekyll website *without* a subpath (such as a GitHub Pages website for a given username):

```yml
baseurl: ""
url: "https://username.github.io"
```

Jekyll website *with* subpath (like the Type on Strap [demo](https://sylhare.github.io/Type-on-Strap/) page):

```yml
baseurl: "/sub-directory"
url: "https://username.github.io/"
```

Please configure this  before using the theme.

### Meta and Branding

Meta variables hold basic information about your Jekyll site which will be used throughout the site 
and as meta properties for search engines, browsers, and the site's RSS feed.

Change these variables in `_config.yml`:

```yml
title: My Jekyll Blog                 # Name of website
avatar: assets/img/triangle.png       # Path of avatar image, to be displayed in the theme's header
description: My blog posts            # Short description, primarily used by search engines
favicon: assets/favicon.ico           # Icon displayed in the tab
```

### Main configuration

#### Footer and Header's text

Customize your site header/footer with these variables in `_config.yml`:

```yml
header_text: Welcome to my Jekyll blog
header_feature_image: assets/img/sample3.png
footer_text: Copyright 2017
```

If you don't want anything, replace the value by `" "`.

#### Localisation string

Localization string is a way to quickly change the template language for text like *Next Post* or *Follow on*, ...
You can find all the properties in `_data/language.yml`.

By default it is in english, but you can easily add your own language.

### Google Analytics

To enable Google Analytics, add your [tracking ID](https://support.google.com/analytics/answer/1032385) 
to `_config.yml` like so:

```yml
google_analytics: UA-NNNNNNNN-N
```

### Comments (via Disqus)

Optionally, if you have a [Disqus](https://disqus.com/) account, you can show a 
comments section below each post.

To enable Disqus comments, add your [Disqus shortname](https://help.disqus.com/customer/portal/articles/466208) 
to your project's `_config.yml` file:

```yml
disqus_shortname: my_disqus_shortname
```

### Math typesetting

When KateX is set in `_config.yml`:

```yml
katex: true # to Enable it
```

You can then wrap math expressions with `$$` signs in your posts and make sure you have set the `katex` variable 
in `_config.yml` to `true` for math typesetting.

For inline math typesetting, type your math expression on the *same line* as your content. For example:

```latex
Type math within a sentence $$2x^2 + x + c$$ to display inline
```

For display math typesetting, type your math expression on a *new line*. For example:

```latex
$$
  \bar{y} = {1 \over n} \sum_{i = 1}^{n}y_i
$$
```

### Social icons

In `_data/social.yml` you can customize the social icons from other wbesite you wish to display in the blog.
The site icons come from [Font Awesome](https://fontawesome.com/).

#### Share in article

The share icons are the one at the bottom of the blog page if enabled, 
to share the article on those platform.


#### Footer

Display  in the footer. 
All icon variables should be your username enclosed in quotes (e.g. "username") in `_config.yml`, 
except for the following variables:

```yml
rss: true                                                   # Make sure you created a feed.xml with feed.xml layout
email_address: type@example.com
linkedin: https://www.linkedin.com/in/FirstLast
stack_exchange: https://stackexchangecom/users/0000/first-last
stack_overflow: https://stackoverflow.com/users/0000/first-last
```

### Customizing Posts

When writing a post, be sure in jekyll to:
 - Put it in the `_posts` folder
 - Name it with the date first like `2019-08-21-This-is-my-blog-post.md`

#### Layout: Post

This are the basic features you can use with the  `post` layout.

```yml
---
layout: post
title: Hello World                                # Title of the page
hide_title: true                                  # Hide the title when displaying the post, but shown in lists of posts
feature-img: "assets/img/sample.png"              # Add a feature-image to the post
thumbnail: "assets/img/thumbnail/sample-th.png"   # Add a thumbnail image on blog view
color: rgb(80,140,22)                             # Add the specified color as feature image, and change link colors in post
bootstrap: true                                   # Add bootstrap to the page
tags: [sample, markdown, html]
---
```

With `thumbnail`, you can add a smaller image than the `feature-img`. 
If you don't have a thumbnail you can still use the same image as the feature one.

The background used when `color` is set comes from `lineart.png` from [xukimseven](https://github.com/xukimseven) 
you can edit it in the config file (`_config.yml > color_image`). If you want another one, put it in `/assets/img` as well. 

The **bootstrap** is not mandatory and is only useful if you want to add bootstrapped content in your page. 
It will respect the page and theme layout, mind the padding on the sides.

#### Post excerpt

The [excerpt](https://jekyllrb.com/docs/posts/#post-excerpts) are the first lines of an article that is display on the blog page. 
The length of the excerpt has a default of around `250` characters and can be manually set in the post using:

```yml
---
layout: post
title: Sample Page
excerpt_separator: <!--more-->
---

some text in the excerpt
<!--more-->
... rest of the text not shown in the excerpt ...
```

The html is stripped out of the excerpt so it only display text.

## Other Layouts
Please refer to the [Jekyll docs for writing posts](https://jekyllrb.com/docs/posts/). 
Non-standard features are documented below.

### Layout: Page

The page layout have a bit more features explained here.

```yml
---
layout: page
title: "About" 
subtitle: "This is a subtitle"   
feature-img: "assets/img/sample.png" 
permalink: /about.html               # Set a permalink your your page
hide: true                           # Prevent the page title to appear in the navbar
icon: "fa-search"                    # Will Display only the fontawesome icon (here: fa-search) and not the title
tags: [sample, markdown, html]
---
```

The hide only hides your page from the navigation bar, it is however still generated and can be access through its link. 

### Layout: Default

This layout includes the head, navigation bar and footer around your content.

## Feature pages

All feature pages besides the "home" one are stored in the `page` folder, 
they will appear in the navigation bar unless you set `Hide: true` in the front matter. 

Here are the documentation for the other feature pages that can be added through `_config.yml`.

### Home

This page is used as the home page of the template (in the `index.html`). It displays the list of articles in `_posts`.
You can use this layout in another page (adding a title to it will make it appear in the navigation bar).

The recommended width and height for the home picture is width:`2484px;` and height:`1280px` 
which are the dimensions of the actual picture for it to be rolling down as you scroll the page.

If your posts are not displaying ensure that you have added the line `paginate: 5` to `_config.yml`.

### Portfolio

Portfolio is a feature page that will take all the markdown/html files in the `_portfolio` folder to create a 3-columns image portfolio matrix.

To use the portfolio, simply create a `portfolio.md` with this information inside:
```yml
--- 
layout: page
title : Portfolio 
---

{% include portfolio.html %}
```

#### Portofolio posts

You can format the portfolio posts in the `_portfolio` folder using the `post layout`. Here are little explaination on some of the possible feature you can use and what they will do.

If you decide to use a date, please be sure to use one that can be parsed such as `yyyy-mm-dd`. You can see more format example on the demo posts that are available for the theme:

```yml
---
layout: post
title: Circus				       # Title of the portfolio post
feature-img: "assets/img/portfolio/cake.png"   # Will display the image in the post
img: "assets/img/portfolio/cake.png"           # Will display the image in the portfolio page
date: 2019-07-25		 	       # Not mandatory, however needs to be in date format to display the date
---
```

#### Portfolio in gem

Make sure your `_config.yml` contains the following if you are using the theme as a gem:

```yml

# PORTFOLIO
collections:
  portfolio:
    output: true
    permalink: /:collection/:name
```    

This creates the collection for Jekyll so it can find and display your portfolio posts.

### Gallery

You can create a gallery using [Masonry JS](https://masonry.desandro.com/) which will placing the pictures in optimal position 
based on available vertical space. 
You need to specify the `gallery_path` which will be used to find the pictures to render. 
It will take all of the picture under that directory. Then use the `include` to add it in your page. 

```yml
---
layout: page
title: Gallery
gallery: "assets/img/pexels"
---

{% include gallery.html gallery_path=page.gallery %}
```


### Search

The search feature is based on [Simple-Jekyll-search](https://github.com/christian-fei/Simple-Jekyll-Search) 
there is a `search.json` file that will create a list of all of the site posts, pages and portfolios. 

Then there's a `search.js` displaying the formatted results entered in the `search.html` page.

The search page can be hidden with the `hide` option. You can remove the icon by removing `icon`:

```yml
---
layout: search
title: Search
icon: "search"
---
```

### Tags

Tags should be placed between `[]` in your post metadata. Separate each tag with a comma. 
Tags are recommended for posts and portfolio items.

For example:

```yml
---
layout: post
title: Markdown and HTML
tags: [sample, markdown, html]
---
```

> Tags are case sensitive `Tag_nAme` ≠ `tag_name`

All the tags will be listed in `tags.html` with a link toward the pages or posts.
The Tag page can be hidden with the `hide` option. You can remove the icon by removing `icon` (like for the search page).

## Advanced

### Liquid tags

Jekyll works with [liquid](https://shopify.github.io/liquid/) tags usually represented by:

```
{{ liquid.tag | filter }}
```

These are useful to render your jekyll files. 
You can learn more about them on [shopify's doc](https://help.shopify.com/themes/liquid/basics)

### Minimizing and optimizing: css, js and images

Before you need to have `node` and `npm` installed:
- Windows: https://nodejs.org/
- Ubuntu/Debian: `apt-get install nodejs npm libgl1 libxi6`
- Fedora (dnf) / RHEL/CentOS (yum): `dnf install node npm libglvnd-glx libXi`

Then you need to install [`gulp-cli`](https://gulpjs.com/) and its dependencies:
```shell
cd assets/
sudo npm install gulp-cli -g
npm install
```

**Now, whenever you want to minify and optimize, run:**
```shell
cd assets/
gulp default
# tip: run a git status to see the changes
git status
```

### Use as Ruby Gem

You can use Type-on-strap as a [gem](https://rubygems.org/gems/type-on-strap). 

Ruby Gem Method
Add this line to your Jekyll site's Gemfile (or create one):

```ruby
gem "type-on-strap"
```
Add this line to your Jekyll site's `_config.yml` file:

```yml
theme: type-on-strap
```

Then run Bundler to install the theme gem and dependencies:

```bash
bundle install
```

Then you can start adding content like:
  - Add a `index.html` file
  - Add the feature page you want. (ex: as it is already in `pages`)
  - Add posts in `_posts` and `_portfolio` to be displayed

### Remote Theme

Now you can use any theme gem with github pages with [29/11/2017 Github Pages Broadcast](https://github.com/blog/2464-use-any-theme-with-github-pages).
For that remove all `theme:` attributes from `_config.yml` and add instead:

```yml
remote_theme: sylhare/Type-on-Strap 
```

## License

There are some fonts and component on this theme going under the MIT licence as well in this theme.
[The MIT License (MIT)](https://raw.githubusercontent.com/Sylhare/Type-on-Strap/master/LICENSE)
