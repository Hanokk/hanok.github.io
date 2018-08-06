---
layout: post
title:  "C++ Essentials"
date:   2018-08-02
categories: c++
---
## Pointers and references:
	 
## Const

* To impose the non modifiability (not entirely refer `const_cast`).
* To restrict the function from modifying, variables are passed as Const.
* Also a function is restricted from modifying any variable by using const in function definition.

	{% highlight c++ %}
	void set(const int var) {
        
	}

	void get() const{

	}
	{% endhighlight %}
	
    -  If we decalre the `set` as const then it wont let us modify 
## Casting:

* static_cast

	{% highlight c++ %}
	{% endhighlight %}

* dynamic_cast:

	{% highlight c++ %}
	{% endhighlight %}

* const_cast:

	{% highlight c++ %}
	{% endhighlight %}

## Operator Overloading:
 * To overload the operation of a operator in the class for customised behaviour of objects.

		{% highlight c++ %}
		void operator+(const& obj){

		}
		{% endhighlight%}

## Inheritance:


## Multi Inheritance:
* If a class is inherited from more than one base class.

## Private Inheritance:

## Abstract Data Types:
* Its analogous to generics or template. In templates we make a method irrespective of data type. Absract data types are custom real world abstract entities
* Like zoo -> elephant,lion
** zoo is abstract data type which for suppose performs actions like area code in which animal is held, type of the animal.
* More like a container that hold set of X. X are the various types in Y. Y is the abstract data type.
* atleast one fucntion should be pure virtual in the abstract class.
** Dog can be a abstract data type where types of dogs can be different class that inherit.

## Friend Class and Functions:
    
## Templates:

* Templates are used when we need a generic implementation irrespective of the data types we pass to a function.

        {% highlight c++ %}
        template <typename T>
        T Myfunc(T x,T y){
            return x>y;
        }
        
        Myfunc<int> (i,j);
    {% endhighlight %}

* Can use either typename or class keyword both are almost same in most of the cases(from C++17 exactly same). its more of a coding style semantic
    
* Compiler can implicitly define the data type we are passing.

        {% highlight c++ %}
        int i,j;
        MyFunc(i,j);
    {% endhighlight %}
    
* class template syntax

        {% highlight c++ %}
        template <typename T>
        class myclassname {
            public:
            T Myfunc(T x,T y){
                return x>y;
            }
        }

        T myclassname<T>::Myfunc(i,j) // if MyFunc not declared inline and instead outside class
    {% endhighlight %}
    
* Suppose there is a special implementation for the diffrent type that we pass we use "Template Specialisation"
** for example we need have a method in class where we call increase which is not applicable for char and we need special requirement to change the case.

        {% highlight c++ %}
        template <typename T>
        class myclassname {
            public:
            T Myfunc(T x,T y){
                return x>y;
            }
        }
        
        template<class T>
        class Myclass {
            T increase (T a){return a++;}
        }
        
        template<>
        class Myclass<char> {
            char uppercase {
                //implement
            }
        }

    {% endhighlight %}
    
## Functors and Functional pointers
* Functors are function objects. `()` operator is oveloaded.

    {% highlight c++ %}
    class func {
        int operator()(int x){ return 2*x}
    }
    
    func fobj;
    fobj(2);
    
    for_each(....,....,func())
    {% endhighlight %}

* They are used to maintain state

        {% highlight c++ %}
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

        {% highlight c++ %}
    (int*) func(int x){
         return 2*x
    }
    
    for_each(....,....,&func)
    {% endhighlight %}
    
* Functions pointers add runtime overhead while functors are inlined during compiled time.

## Lambda Expression

* Lanbda expression are also called anonymous functions of functional language and its similar to functor but less code and no state

        {% highlight c++ %}
    auto f = [](int x){return 2*x;};
    {% endhighlight %}
* More on this here.