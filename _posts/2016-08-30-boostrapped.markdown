---
layout: post
title: "Bootstrapped"
date: 2016-08-30 09:42:57 -0400
comments: true
categories:
---



Part of the most recent project, Junket Journeys, made me want to look into making my website not only functional but to look nice. Building my own CSS styles for a site can take a while, luckily there are ways to use pre-created builds to develop this site. Bootstrap is a popular version of this kind of framework and they don't have a problem saying so:

![boot](/assets/bootstrapped/bootstrap.png)

I don't really have a problem with it though. It's a fantastic tool that's easy to use and customizable.

It takes you from this   
![George mf Burns](/assets/bootstrapped/burns.gif)   
To this:   
![Pete Webber](/assets/bootstrapped/bowling.gif)   
In less than an hour. OK so how do you do that? In your project gemfile add the `bootstrap-sass` gem.

Next in your `app/assets/stylesheets/application.scss` add:
``` css
@import "bootstrap-sprockets";
@import "bootstrap";
```
Next in your `app/assets/javascripts/application.js` add:
``` javascript
//= require jquery
//= require bootstrap-sprockets
```

That's it. 5 lines of code and your website can go from text on a page to a fully fledged website.

![Basic Site](/assets/bootstrapped/shit_website.png)

To implement any sort of bootstrap on your website you can simply go to the bootstrap site and pick the elements that you'd like. A quick solution to change your site is to go to [Bootswatch](https://bootswatch.com/) and find a theme that you like. When you find something that you like you can view the source code and copy the CSS into your project. Create a file in your `app/assets/stylesheets/` with a .CSS filename and copy this code into it. Go back into your `app/assets/stylesheets/application.scss` file and add an `@import "FILENAME";` to the document. Refresh your site and you'll see a completely new look!

Additionally you can copy the information from the Bootstrap website that you'd like to use. This is something that can help you with both the visuals of your site and the layout. By including specific class names on your objects you can inherit the layout and design included in bootstrap.

For example:
``` css
class="btn btn-warning"
class="btn btn-danger"
```
Give you two different looking buttons -
![web example](/assets/bootstrapped/buttons.png)

Additionally you can set how your elements are displayed on your page. Bootstrap operates on a 12 column [grid system](http://getbootstrap.com/css/#grid). By including the appropriate class tag on your html files you can place them within this column structure. Naming your class `col-md-4` makes that object 1/3 the width of the screen. You can offset your items from the edge of the screen using this same column structure. In fact wrapping the `<% yield %>` statement in your main application layout with a class of 'container' helps frame your website really well. There are a ton of options that come along with bootstrap that allow you to make changes through simple naming conventions or by copying the available code from the bootstrap website.

![Bob Ross](/assets/bootstrapped/bob.ross.gif)
