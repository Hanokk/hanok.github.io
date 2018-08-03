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
    *Templates are used when we need a generic implementation irrespective of the data types we pass to a function.
    **Eg:
        {% highlight ruby%}
        template <typename T>
        T Myfunc(T x,T y){
            return x>y;
        }
    {% endhighlight %}

## Functors and Functional pointers
    * Functors are function objects. _() operator is oveloaded
    **Eg:
    {% highlight ruby%}
    class func {
        int operator()(int x){ return 2*x}
    }
    
    func fobj;
    fobj(2);
    
    for_each(....,....,func())
    {% endhighlight %}

    * They are used to maintain state
    **Eg:
        {% highlight ruby%}
    class func {
        int local;
        func(y){
            local = y;
        }
        int operator()(int x){ return x*local}
    }
    
    func fobj(5);
    fobj(2);
    
    for_each(....,....,func(5))
    {% endhighlight %}
    
    * Function pointers
    **Eg:
        {% highlight ruby%}
    (int*) func(int x){
         return 2*x
    }
    
    for_each(....,....,&func)
    {% endhighlight %}
    
    * Functions pointers add runtime overhead while functors are inlined during compiled time.