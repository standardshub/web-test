# Example demo site

This repository demonstrates how to deploy a static website on AWS S3. If you
are web designer please read this README. If you would like to know how to
deploy, read [docs/README.md](docs/README.md).

The staging site URL is
http://starhub-demo.s3-website-ap-northeast-1.amazonaws.com/

http://mywebtest.s3-website-us-west-1.amazonaws.com/

## Requirements

* ruby (2.6, or at least 2.4)
* bundler (see https://bundler.io/ for installation)
* git

## Install

First, fork the repository on GitHub.

Next, checkout _your_ repository (replace `CHANGEME` with your GitHub ID).

```console
> git clone https://github.com/CHANGEME/jekyll-site-demo-starhub.git

```

All command after this command should be in the repository directory.


```console
> cd jekyll-site-demo-starhub
```

Install gems.

```console
> bundle install --path=vendor/bundle
```

## Run the demo server on local machine

```console
> bundle exec jekyll s
Configuration file: /usr/home/trombik/github/trombik/jekyll-site-demo-stathub/_config.yml
            Source: /usr/home/trombik/github/trombik/jekyll-site-demo-stathub
       Destination: /usr/home/trombik/github/trombik/jekyll-site-demo-stathub/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
       Jekyll Feed: Generating feed for posts
                    done in 0.345 seconds.
  Please add the following to your Gemfile to avoid polling for changes:
    require 'rbconfig'
    if RbConfig::CONFIG['target_os'] =~ /(?i-mx:bsd|dragonfly)/
      gem 'rb-kqueue', '>= 0.2'
    end
 Auto-regeneration: enabled for '/usr/home/trombik/github/trombik/jekyll-site-demo-stathub'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

The demo URL is [http://127.0.0.1:4000/](http://127.0.0.1:4000/).

## Spell check in CI

One of GitHub Actions includes spell checking by `aspell`. The action will run
on every push. It checks all `.markdown` files in the repository. When you
know words `aspell` complains about are correct, add the words to
`.aspell.en.pws`, which is a personal word list, at the root directory. The
words will be white listed.

## Reporting bugs or requesting new features

Report issues, or feature requests in `Issues`. When create an issue, you need
to choose the type of the issue, which includes:

- Bug report
- Feature request
- Question

The repository contains a set of templates for bug report, feature request,
etc. Please read comments in the templates and follow the instructions when
you create one.
