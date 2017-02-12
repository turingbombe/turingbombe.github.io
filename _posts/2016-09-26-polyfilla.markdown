---
layout: post
title: "Polyfilla"
date: 2016-09-26 23:44:23 -0400
comments: true
categories:
---

So before I jump into this post on Polyfilla's a quick bit of background on their origin. Flash back to 2007 and the development world is awaiting the release of ECMAScript 4. This is the first major update to JavaScript that promises to being fortha series of significant updates to the language of the web... things kind of take a turn here. Several large members of the ECMAScript commitee have issues with ES4 and the whole this eventually abandoned. Later this group sets out to develop an ECMAScript update that they (ES5) in 2009. That's 10 years after the last major update..   

Just to give you a quick look at what happened to websites during that time we can see the info below:

Microsoft's Website in 1999:
![MS 1999](/assets/polyfilla/microsoft.1999.png)

Microsoft's Website in 2009:
![MS 2009](/assets/polyfilla/microsoft.2009.png)

So in this same 10 year time frame there were 2 major updates to Internet Explorer. In the 8 years following this there have been 5 major updates to IE which you all have been enjoying...

So where does this leave us? Well for 'us' as developers we probably don't have issues updating our browsers, but *others* might lag behind. The chart below shows how that can impact what we're doing.
![Support](/assets/polyfilla/browser.support.png)

After such a large gap in updates ECMAScript is supposed to be updated more routinely and can create even more frequent gaps in what is being created and what can be viewed.

So for every Bill there will be plenty of Hillary's online as well...
![Shock](/assets/polyfilla/clintons.gif)

This is where Polyfills come in. They exist to make features available on older browsers that are beyond the browser's capabilities. These workarounds allow us to keep improving web features while taking care of all internet users.

Some library's, like Modernizr, collect each of these polyfills or shims in a central place and allow you to implement them throughout your code.

There are some locations where they collect this information and allow you to check what you are able to bring to older browsers with polyfills, such as [HTML5 Please](http://html5please.com/). Babel is a transpiler that you can use to get ES6 working on older browsers, but there are things like [ES6 Shim](https://github.com/paulmillr/es6-shim) that you can also use to add these features to your page.

As things keep on progressing on the web there will be many laggards and many more people that are simply using whatever devices they have available to them. Consistency is a constant issue in web development, hopefully these kinds of programs can help to make sure people are able to experience the web in the way we develop it.
