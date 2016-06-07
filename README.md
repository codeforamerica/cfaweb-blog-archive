What is this
============

This repository holds an archive of Code for America blog posts between 2010 (when we first started a blog) to mid-2016. The posts are wrapped up in a simple static website generator that formats them and turns them into nice HTML pages.

### Why we have a blog archive

In 2016, the Code for America Marketing/Communications team lead a content strategy focused redesign of the Code for America website. During the redesign, the team made the decision to leave behind our past website platform and move to a new one. During the migration, we also chose to not move over every single piece of content to our new blog, now [hosted on Medium](https://medium.com/code-for-america). Some important posts were moved over and reformatted, and the rest were exported from WordPress and put into this simpler-to-maintain system. With no database, and just a simple HTML site output, this blog archive should require *little to not maintenance* after it is put up.


How do I use it
===============

The archive is a simple Jekyll-based static site. To deploy it locally, you'll need to configure your environment, download the application dependencies, and use Jekyll to build the site.

### How to deploy it locally

#### 1. Environment
First, you'll need to [install Ruby (instructions here)](https://github.com/codeforamerica/howto/blob/master/Ruby.md). This application also requires the following:

* [Ruby](https://www.ruby-lang.org/en/) version 2.2.0
* [RubyGems](https://rubygems.org/pages/download])
* [Bundler](http://bundler.io/)
* [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

#### 2. Application

Next, you can clone the Github repository locally and install the application dependencies. You can run these commands in your shell to get started:

```
# Clone the repository using Git
$ git clone https://github.com/codeforamerica/cfaweb-blog-archive.git

# Install necessary gems using Bundler
$ bundle install

# Build the site and serve it
$ bundle exec jekyll serve
```

#### 3. Using Jekyll

Read more about using [Jekyll in this official guide](https://jekyllrb.com/docs/quickstart/). Here are a few basic commands to get you started with Jekyll:

```
# Just build the site
$ bundle exec jekyll build

# Build the site and serve it
$ bundle exec jekyll serve

# Build the site, serve it, and watch for saved changes then rebuild
$ bundle exec jekyll build
```

How it's hosted on the internet
===============================

#### 1. Hosting: Amazon S3

The final, built site is deployed on an Amazon S3 Bucket [configured to serve a static website](http://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html). It is hosted on the Code for America AWS account in the bucket `cfa-static-blog-archive`. The DNS pointing to it is managed separately by the Code for America website infrastructure.

#### 2. Deployment: s3_website and Travis CI

The [s3_website gem](https://github.com/laurilehmijoki/s3_website) is used to easily deploy the website to S3 after changes are made. You can deploy the site locally by copying `.env.example` to `.env` and providing an AWS IAM key and secret that has access to the `cfa-static-blog-archive` bucket. [Here is the s3_website guide to setting up the correct credentials.](https://github.com/laurilehmijoki/s3_website/blob/master/additional-docs/setting-up-aws-credentials.md).

Travis CI is used for continuous deployment. Travis automatically builds and deploys the master branch every time it is pushed to the Github repo. The correct AWS credentials are stored as environemnt variables on Travis.

Copyright and license
=====================
Copyright Code for America Labs, 2016 and released under the MIT License.
