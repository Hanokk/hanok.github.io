---
layout: post
title:  "Python tidbits"
date:   2018-07-31
categories: Python
---

## Conditional flows
	* No switch statements instead only if-else.
	**Eg:
	{% highlight py %}
	if a:
	elif b:
	else:
	{% endhighlight %}
	* for statement:
	**Eg
	* for exhaustion can transfer control to else
	{% highlight py %}
	for w in range(5):
		print w
	else:
		print ""

	{% endhighlight %}

##Functions
	*functions call can have fewer arguments to pass than the actual definition if the function definition has as default value to pass.
	**Eg
	{% highlight py %}
	def funct(a,b=2,c=3):
		print(a,b,c);
	{% endhighlight %}1

##New
	* in : if a value is present in the sequence (more to explore)
## Built-ins
	**range - Iterator

