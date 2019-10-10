---
title: How to build an API docs site using Slate
date: '2018-12-10T06:01:00.812Z'
excerpt: >-
  If you want to build a simple but attractive looking API documentation site,
  you can’t really go wrong with an open-source tool like Slate…
thumb_img_path: images/How-to-build-an-API-docs-site-using-Slate/1*NMCPwETJJL7-pIy4XCitYA.png
layout: post
---
![](/images/How-to-build-an-API-docs-site-using-Slate/1*NMCPwETJJL7-pIy4XCitYA.png)

If you want to build a simple but attractive looking API documentation site, you can’t really go wrong with an open-source tool like [Slate](https://github.com/lord/slate). Despite being created by a teenager developer during a summer internship, it has become an incredibly popular tool with the project being forked more than 15,000 times and with well-known organisations including [NASA](https://api.nasa.gov/index.html), [Best Buy](https://bestbuyapis.github.io/api-documentation/), [Monzo](https://docs.monzo.com/#introduction) and [Skyscanner](https://skyscanner.github.io/slate/?_ga=1.104705984.172843296.1446781555#api-documentation) all using it.

### 🎬 So what is Slate?

Slate is a Ruby-based tool that generates a great-looking, three-panelled API documentation static site from a set of markdown files. It was built by developer Robert Lord in 2013 when he was an 18-year-old intern at at travel software company Tripit. He convinced his boss at the time to let him open-source the project and the rest is history.

[He said he found it pretty surreal](https://documenter.co.uk/2018/06/18/a-clean-slate-the-story-behind-an-api-docs-tool/) that so many people were now using and maintaining his “buggy project” nearly six years later. However, the results speak for themselves — you can see some examples in the [Slate in the Wild](https://github.com/lord/slate/wiki/Slate-in-the-Wild) repository.

### 🛠️ Before you begin

So before you begin, make sure you have met the following requirements:

*   You have an Open API/ Swagger file in .yaml or .json format.
*   You have installed [Node.js](https://nodejs.org/en/). This includes npm (Node Package Manager).
*   You have installed [swagger-to-slate](https://www.npmjs.com/package/swagger-to-slate) or [widdershins](https://github.com/mermade/widdershins) (or similar) to convert your file into Markdown. I used the former in this example.
*   You have installed Vagrant and VirtualBox.

In this example, I’m going to use the generic [Swagger Petstore example](https://editor.swagger.io/) which I have saved to my Desktop and called petstore.yaml. To convert this to Markdown using `swagger-to-slate`, open a terminal and run:

    `swagger-to-slate -i /Users/james.scott/Desktop/petstore.yaml`

This saves a file called petstore.md in the same location as the .yaml file. Once you have this, you can get started with Slate.

### 🔨 Build your site using Vagrant

To build your API documentation site using Vagrant, follow these steps:

1.  Go to the [Slate](https://github.com/lord/slate) repository on Github.
2.  Click **Fork** to create your own fork of the main repository.
3.  Clone your fork to your local machine using `git clone`. For example:`git clone [https://github.com/<your_github_username>/slate.git](https://github.com//slate.git)`
4.  Go to `~/slate/source` and remove the index.html.md file.
5.  Rename the Markdown file you created earlier as index.html.md and copy it into the source folder, changing the file locations as required:  
    `cp ~/<local_path>/index.html.md ~/<local_path>/slate/source/`
6.  To build your site using Vagrant, run: `vagrant up`
7.  Go to [http://localhost:4567](http://localhost:4567) to see your site. It may take several minutes to build and appear.

### 🐳 Build your site using Docker

You can also use Docker to create your site but you must edit some additional files. Although this method is not officially supported, I had no issues when I tried using it.

If you are using Ruby version 2.5.1 or newer, you need to create three files:

*   .dockerignore :

    .git   
    source

*   Dockerfile :

    `FROM ruby:2.5.1  
    MAINTAINER Adrian Perez <adrian@adrianperez.org>  
    VOLUME /usr/src/app/source  
    EXPOSE 4567  
      
    RUN apt-get update && apt-get install -y nodejs \  
    && apt-get clean && rm -rf /var/lib/apt/lists/*  
      
    CMD ["bundle", "exec", "middleman", "server", "--watcher-force-polling"]`

*   docker-compose.yml :

    app:  
      build: .  
      ports:  
        - 4567:4567  
      volumes:  
        - ./source:/usr/src/app/source

Add these files to your local Slate directory.

To build your Docker site run: `docker-compose up`

You should be able to see your site at [http://localhost:4567](http://localhost:4567).

For alternative Docker methods refer to [this documentation](https://github.com/lord/slate/wiki/Docker).

### 💎 Build your site using Bundler

Alternatively, if you want to run your Slate site locally, you can also use Bundler. To use this method you must install Ruby version 2.3.1 or newer. To check which version you have installed run: `ruby -v`

If you need to install Ruby see the [installation documentation](https://www.ruby-lang.org/en/documentation/installation/) for the different methods available.

Once installed, you can install Bundler: `gem install bundler`

To build your API docs site using builder:

1.  Navigate to your Slate directory: `cd slate`
2.  Install the dependencies such as [Middleman](https://middlemanapp.com/) specified in the Slate Gemfile: `bundle install`
3.  Launch the Middleman static site generator: `bundle exec middleman server`
4.  Go to [http://localhost:4567](http://localhost:4567) to see your site.

That’s pretty much it! Good luck.
