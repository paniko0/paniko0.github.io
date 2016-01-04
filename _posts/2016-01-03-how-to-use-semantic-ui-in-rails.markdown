---
layout: post
title:  "How to use semantic-ui in rails"
date:   2016-01-03 21:35:00 -0200
categories: semantic rails
---
I've been using [semantic-ui](http://semantic-ui.com/) on some rails project and it's a good UI framework to work with because of it's social clean and flex design.

But to I didn't find any blog post on how to use it in a rails app. When we talk about stylesheet frameworks, the first thing that comes into our mind is Bootstrap or Foundation, with their tons of tutorials and gems on how to use on a rails project and the problem is that I don't find the same amount of information when we talk about semantic, even it seems so easy to understand.

- The first thing we have to do is download [semantic.js](https://raw.githubusercontent.com/Semantic-Org/Semantic-UI-CSS/master/semantic.js) and [semantic.css](https://raw.githubusercontent.com/Semantic-Org/Semantic-UI-CSS/master/semantic.css)

- We are going to put `semantic.js` on `vendor/assets/javascripts` and `semantic.css` on `vendor/assets/stylesheets`

- Configure your rails app to use semantic files changing `config/initializers/assets.rb` adding:

{% highlight ruby %}
  Rails.application.config.assets.precompile += %w( semantic.css semantic.js )
{% endhighlight %}

- Finally, we just have to change `application.js` file adding:
{% highlight ruby %}
  //= require semantic
{% endhighlight %}

and application.css adding:
{% highlight ruby %}
  *= require semantic
{% endhighlight %}

and here we are, with all files configurated and ready to be used.
