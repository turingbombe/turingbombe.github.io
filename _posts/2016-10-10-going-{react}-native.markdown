---
layout: post
title: "Going {React} Native"
date: 2016-10-10 22:54:03 -0400
comments: true
categories:
---

After spending a little over a week working in React I grew intrigued by React Native and wanted to understand it a little better. I mean, why not? Right?

![Good Choices](/assets/going-native/crocodile.jpg)

React Native is a Javascript framework, based on React, used to develop native applications. We're not talking web apps here, these are fully integrated *native* apps. I don't know the first thing about writing iOS or Android apps but I'm definitely into the idea some of the web apps I've worked on to a mobile device. Since I'm learning React, this seems like as good a place as any to start.

So let's take a look at the ubiquitous starter app...

{% highlight javascript %}
import React, { Component } from 'react';
import { AppRegistry, Text } from 'react-native';

class HelloWorldApp extends Component {
  render() {
    return (
      <Text>Hello world!</Text>
    );
  }
}

AppRegistry.registerComponent('HelloWorldApp', () => HelloWorldApp);
{% endhighlight %}

![BOWIE](/assets/going-native/bowie.gif)

Wow... OK so this is actually a thing. React Native really does build in the principles of React on top of the native environment. There are still some components of the native environment that have to be understood. For example `AppRegistry` is an item I'd not encountered before. I like to think of this as the `ReactDOM` of the native environment.

The React Native library also incorporates other elements of React that should be familiar. `Props` are available within components and `state` still manages your application, so the skeleton is there for you to build with. Obviously there are many differences but the core concepts remain unchanged, which is a really nice way to walk into a new programming space.

A few easy differences can be seen in the way that data is rendered/returned. For example `<Text>` tags encapsulate the text in our earlier app. More commonly `<View>` tags outline the return in a similar manner to `<div>` tags that surround React returns.

A React Native element that can really be appreciated is the inclusion of Flexbox. Flexbox allows you create pieces your app that adapt to work on any sized screen. So whether you're Galaxy Note 7 is exploding or you're unable to listen to music on your new iPhone the screen will be displayed correctly! Try changing the flexDirection in the link below and playing with the width/height values.

{% raw %}
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="880" height="425" src="https://cdn.rawgit.com/dabbott/react-native-web-player/v1.2.4/index.html"></iframe>
{% endraw %}

These are just some of the things I've found fascinating about React Native. Certainly enough to keep me digging deeper into using this. Next time I will dig into React Native in even more detail
