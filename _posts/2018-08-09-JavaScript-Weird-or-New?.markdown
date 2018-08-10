---
layout: post
title:  "JavaScript: Weird or New!"
date:   2018-08-09
categories: [Javascript,functional]
---

* Things i want in any laguage or anyone for that matter is simplicity, readability, reducing the coding time and promote rapid developement and special trait that a language has that i can leverage on for some particular level development.

* My first impressions on JavaScript being weak typed and dynamically typed makes the less verbose. In JS almost everything is Object except those primitive data types(Boolean, Number etc).

* Some of the ways to declare objects. All the objects are treated as key value pair.

{% highlight js  %}
    var obj = new Object();

    var obj = {};
{% endhighlight %}

{% highlight js %}
    var user = {name : "", age : 25};
    
    user.name or user['name']
{% endhighlight %}

* Functions are also objects. And supoorts fucntional programming features like first class functions where function can be treated as variable which can be initialised
with function, passed into a fucntion and can return fucntion.

{% highlight js %}
    var func = function (){
        return "Hello";
    }
{% endhighlight %}

{% highlight js %}
    function func(){
        return "Hello";
    }
{% endhighlight %}

{% highlight js %}
    var func = {}=>{
        return "Hello";
    }
{% endhighlight %}

{% highlight js %}
    function func(){
        return function(){
            return "Hello"
        };
    }
    
    var a = func();
{% endhighlight %}

* Closures are also supported. In JS scope is function level and each function initialisation creates a object corresponding to the function and it will be accessed
by all the functions nested inside the function. Every new function creates an object corresponding to that function.

{% highlight js %}
    function func(){
        var c = "closure";
        return function(){
            return c;
        }
    }
{% endhighlight %}
