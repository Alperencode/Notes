# Python Decorators

In Python, functions are first class objects, that mean the functions in Python can be used or passed as arguments. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The decorators are used to modify the behaviour of function or class. 
A decorator is a function that takes another function as an argument, does some actions, and then returns the argument based on the actions performed.

<br>

## Basic Syntax and Problems

They are usually called as wrapper in the decorator function but of course it can be whatever you need.


```python
def mydecorator(function):
    
    def wrapper():
        print("Wrapper called") 
        function()
    
    return wrapper

@mydecorator
def helloWorld():
    print("Hello World")

helloWorld()
```
Output:
```
Wrapper called
Hello World
```

<br>

This is the basic usage of decorators
but when we try to pass arguments there is some problems we're going to face. 
Because if we try to take arguments for helloWorld function we need to take same arguments in wrapper but its obviously not something we want to do everytime.
So we basically just giving it *args and **kwargs to prevent this problem.
So we can pass as many argument as we need.

<br>

For an example:

```python
def mydecorator(function):
    
    def wrapper(*args,**kwargs):
        print("Wrapper called") 
        function(*args,**kwargs)
    
    return wrapper

@mydecorator
def helloWorld(name):
    print(f"Hello {name}")

helloWorld("Alperen")
```
Output:
```
Wrapper called
Hello Alperen
```
<br>

## Chaining Decorators

Its basically chaining more than one decorators.
When we chain the decorators the order is being from top to bottom.

<br>

For an example:

```python
def star(func):
    def inner(*args, **kwargs):
        print("*" * 30)         # (Step 1)
        func(*args, **kwargs)   # (Step 2)
        print("*" * 30)         # (Step 7)
    return inner


def percent(func):
    def inner(*args, **kwargs):
        print("%" * 30)        # (Step 3)
        func(*args, **kwargs)  # (Step 4)
        print("%" * 30)        # (step 6)
    return inner


@star
@percent
def printer(msg):
    print(msg)         # (Step 5)


printer("Hello")
```

Output of this code:
```
******************************
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
Hello
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
******************************
```

So this code following the steps that i stated. As you can see It's starting from the first decorator we mentioned on top then goes to bottom.

<br>

## Why do we need decorators?

It is simple: readability. 
Python is praised for its clear and concise syntax, and decorators are no exceptions.
If there is any behaviour that is common to more than one function, you probably need to make a decorator.