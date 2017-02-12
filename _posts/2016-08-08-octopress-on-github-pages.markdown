---
layout: post
title: "Octopress on Github Pages"
date: 2016-08-08 09:23:45 -0400
comments: true
categories:
---
I recently set up this blog using Octopress as a way to track things I've found interesting or helpful as I start coding more and more. I realized shortly after that setting up this blog was something that I searched for help on but still ran into a few roadblocks.

### Why did I choose Octopress?
I'm sure there are several other sources out there, I know that WordPress, Tumblr, and Hugo are just a few that I know people use. I went with Octopress for a few reasons.

1. Setting up the blog was something new to learn
2. Customizing the blog may be something that I want to do in the future
3. Centralizing information on GitHub

### Setting up the blog
OK, so now onto the important stuff. How do you set up Octopress to work with GitHub pages?

First, you need to set up your GitHub pages site. Simply go to your gitub page and create a new repository named `<username>.github.io` where <username> is your _exact_ username. That's it. We're not going to run any git commands on this, we'll just come back for our SSH link.

Now we can set up Octopress. There are a few dependencies so let's get that going.
_NOTE_: The code below sets up the folder that your blog will be housed in. You can replace `octopress` with other folder names in the first line if you want it to be saved under a different name.

{% highlight bash %}
git clone git://github.com/imathis/octopress.git octopress
cd octopress
{% endhighlight %}

Great so now you have the bare bones of your blog but we need a few more things. Go into your `octopress` folder and run `bundle install` to get all of your dependencies. One more command... `rake install` and you should have your blog set-up with the default Octopress theme.

### Linking with GitHub Pages
Linking up your GitHub page is fairly simple as Octopress has a command set up for you to do this 
{% highlight bash %}
rake setup_github_pages
{% endhighlight %}

You will be asked for the url of your GitHub repo, so copy and paste that from your site (e.g. `git@github.com:username/username.github.io.git`).

If you want to find out more about what this does for you, take a look on the [Octopress site](http://octopress.org/docs/deploying/github/ "Octopress").

To get everything generated run:

{% highlight bash %}
rake generate
rake deploy
{% endhighlight %}

OK, so things should be good to go. Now one time you need to push this newly generated site to GitHub:

{% highlight bash %}
git add .
git commit -m 'your message'
git push origin source
{% endhighlight %}

### Creating _Your_ Blog
OK, take a deep breath. Your blog is up, well not quite. _A_ blog is up, a generic, contentless, shell of a blog. Here's how to make it **yours**.

Let's get your blog name up there and some other general details. In your main blog folder there is a `_config.yml` file that contains most of your general blog settings. Open that up in your text editor of choice and it should start with the following:
{% highlight yaml %}
# ----------------------- #
#      Main Configs       #
# ----------------------- #

url: http://yoursite.com
title: My Octopress Blog
subtitle: A blogging framework for hackers.
author: Your Name
simple_search: https://www.google.com/search
description:
{% endhighlight %}

Change the information in here to match what you'd like for your own blog. There are many more settings/plugins that you can configure. But I'm not going to get into that here.

Once you're all set run `rake new_post["(POST NAME)"] will generate a new post document for you. You can open up this file and start blogging away. Every time you've finished a post, simply repeat the following tasks

{% highlight bash %}
rake generate
rake deploy
{% endhighlight %}

And you're good to go, that's how this got here..
