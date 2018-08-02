---
layout: post
title:  "C++ Essentials"
date:   2018-07-31
categories: c++
---
##Pointers and references:
	* 
##Const:
	* To impose the non modifiability (not entirely refer const_cast)
	* To restrict the function from modifying, variables are passed as Const.
	* Also a function is restricted from modifying any variable by using const in function definition
	**Eg:
	{% highlight ruby %}
	void set(const int var) {

	}

	void get() const{

	}
	{% endhighlight %}
##Casting:
	*static_cast:
	**Eg:
	{% highlight ruby %}
	{% endhighlight %}

	*dynamic_cast:
	{% highlight ruby %}
	{% endhighlight %}

	*const_cast:
	{% highlight ruby %}
	{% endhighlight %}

##Operator Overloading:
	* To overload the operation of a operator in the class for customised behaviour of objects.
	** Eg:
		{% highlight ruby %}
		void operator+(const& obj){

		}
		{% endhighlight%}
##Inheritance:


##Multi Inheritance:
	* If a class is inherited from more than one base class.
##Private Inheritance:

##Abstract Data Types:


##Friend Class and Functions:

##Templates:
