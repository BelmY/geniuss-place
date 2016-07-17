---
title: "How to contribute"
permalink: /contribute/
excerpt: "Contributing to the Source Code"
modified: 2016-06-22T15:54:02-04:00
header:
  teaser: "geniuss-contribute.png"
comments: true
---
{% include base_path %}
{% include toc %}

![Contributing]({{ site.url }}{{ site.baseurl }}/images/geniuss-contribute.png){:height="250px" width="250x"}


## Contributing to GNSS-SDR

Found a bug in the code? Interested in adding a new feature or [fixing a bug](https://github.com/gnss-sdr/gnss-sdr/issues)? Then by all means [submit an issue](https://github.com/gnss-sdr/gnss-sdr/issues/new){:target="_blank"} or [pull request](https://help.github.com/articles/using-pull-requests/){:target="_blank"}. If this is your first pull request, it may be helpful to read up on the [GitHub Flow](https://guides.github.com/introduction/flow/){:target="_blank"} first. If you need a quick introduction to Git and its parlance (concepts such as _repository_, _commit_, _push_, _pull-request_, etc.), check our [Git tutorial]({{ site.url }}{{ site.baseurl }}/docs/tutorials/using-git/).

[<i class="fa fa-github fa-lg"></i> Fork GNSS-SDR from GitHub](https://github.com/gnss-sdr/gnss-sdr/fork){: .btn .btn--notice .btn--x-large}
{: style="text-align: center;"}

Before start working in GNSS-SDR source code, specially if you want to contribute your changes back to the _upstream_ repository, you may be interested in having a look at our [coding style guide]({{ site.url }}{{ site.baseurl }}/coding-style/).

## Contributing to this website

Found a typo in this website? Interested in giving your thoughts on existing pages, adding a post, tutorial, new feature or enhancement?

This website itself lives in a [GitHub repository](https://github.com/carlesfernandez{{ site.baseurl }}/){:target="_blank"}.

 * Comment (through your Google, Facebook or Twitter account, or just open a new profile at [Disqus](https://disqus.com/){:target="_blank"}) in the boxes such as the one at the bottom of this page. Moderation will be applied only in cases of flagrant off-topic or unappropriate style.

 * Check [existing open issues](https://github.com/gnss-sdr/gnss-sdr/issues/){:target="_blank"} or submit a [new one](https://github.com/gnss-sdr/gnss-sdr/issues/new){:target="_blank"}.

 * [Fork this web](https://github.com/carlesfernandez{{ site.baseurl }}/fork){:target="_blank"}, work on the changes in your own repository, and make a pull request.

 [<i class="fa fa-github fa-lg"></i> Fork this website from GitHub](https://github.com/gnss-sdr/gnss-sdr/fork){: .btn .btn--notice .btn--x-large}
 {: style="text-align: center;"}


## How to run this website locally

The required software can be installed through [RubyGems](https://rubygems.org/){:target="_blank"}, which is probably already installed in your system.

Install [Jekyll](https://jekyllrb.com/){:target="_blank"}:

```bash
$ sudo gem install jekyll
```

More information at [Jekyll's installation page](https://jekyllrb.com/docs/installation/){:target="_blank"}. Then, install [Bundler](http://bundler.io/){:target="_blank"}, a tool for managing the required dependencies:

```bash
$ sudo gem install bundler
```

Clone your forked repository of this website and install the required dependencies:

```bash
$ git clone https://github.com/YOUR_USERNAME/test/
$ cd test
$ bundler install
```

After all gems are installed, the following command will deploy the website and run a local server at http://127.0.0.1:4000/

```bash
$ bundle exec jekyll serve -w --config _config.yml,_config.dev.yml
```

Just point your browser to that local direction in order to enjoy this website without the need of Internet connection. Some features such as comments might not work.

**Pro Tip**: if you want to modify Stylesheets or JavaScript (under ```/assets/_scss``` and ```assets/js```, respectively), you will need to install [Node.js](https://nodejs.org/en/){:target="_blank"}, ```cd```to the root of your project, and run ```$ npm install``` to get all the dependencies. If all goes well, running running ```$ npm run build:css``` will process all SCSS files into ```main.css```. and ```npm build:js``` will compress/concatenate ```_main.js``` and all plugin scripts into ```main.min.js```. Thus, upon a change on css or JavaScript content, run:
```
$ npm run build:css
```
or
```
$ npm run build:js
```
in order to update ```main.css``` and ```main.js``` scripts and implement the changes on the website.
{: .notice--warning}

**Note**: If you upgraded from a previous version of the theme be sure you copied over ```package.json``` prior to running ```npm install```.
{: .notice--warning}