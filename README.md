Ihor
====

Minimalistic [Hugo](https://gohugo.io) theme with responsive design and semantic markup. Provides integration with [Disqus](https://disqus.com/), Google Analytics and highlights code using [prism.js](http://prismjs.com/).

### Example

Have a look at my personal website [ihor.burlachenko.com](http://ihor.burlachenko.com/) to see how the theme looks like. The sources are [here](https://github.com/ihor/ihor.burlachenko.com).

### Installation

```
$ cd your_site_repo/
$ mkdir themes
$ cd themes
$ git clone https://github.com/ihor/IhorHugo ihor
```

See the [official Hugo themes documentation](http://gohugo.io/themes/installing) for more info.

### Usage

This theme expects a relatively standard Hugo blog/personal site layout:
```
.
└── content
    ├── post
    |   ├── post1.md
    |   └── post2.md
    ├── license.md  // this is used in the footer link
    └── about.md    // this is used in the about page
```

Just run `hugo --theme=ihor` to generate your site!

### Configuration

An example of what your site's `config.toml` could look like. All theme-specific parameters are under `[params]` and standard Hugo parameters are used where possible.

``` toml
baseurl = "http://example.com/"
title = "Your site title"
languageCode = "en-us"
disqusShortname = "your_disqus_shortname" # Optional, enable Disqus integration
MetaDataFormat = "toml"
theme = "ihor"
paginate = 10

[author]
    name = "Your Name"

[permalinks]
    # Optional. Change the permalink format for the 'post' content type.
    # The format shown here is the same one Jekyll/Octopress uses by default.
    post = "/blog/:year/:month/:day/:title/"

[taxonomies]
    # Optional. Use if you want tags and lists.
    category = "categories"

#
# All parameters below here are optional and can be mixed and matched.
#
[params]
    # If false display full article contents in blog index.
    # Otherwise show description and 'read on' link to individual blog post page.
    # Default (if omitted) is true.
    truncate = true

    # Used when a given page doesn't set its own.
    defaultDescription = "Your default page description"
    defaultKeywords = "your,default,page,keywords"

    # Hide estimated reading time for posts.
    # Default (if omitted) is false.
    hideReadingTime = false

    # Select a syntax highight.
    # Check the static/css/highlight directory for options.
    highlight = "sunburst"

    # Optional additional custom CSS file URL, will override other styles.
    customCSS = ""

    # Displays under the author name in the header, keep it short.
    # You can use markdown here.
    tagline = "Your favourite quote or soundbite."

    # Metadata used to drive integrations.
    googleAnalytics = "Your Google Analytics tracking code"

    # Pinterest
    pinterestVerify = "Your Pinterest verification code"

    # Header social links, these must be full URLs.
    github = ""
    bitbucket = ""
    stackOverflow = ""
    linkedin = ""
    googleplus = ""
    facebook = ""
    twitter = ""
    youtube = ""
    email = ""
```
