# Functional Programming

## What is functional programming?
a style of building the structure and elements of computer programs that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data
## What is a pure function and how do we know if something is a pure function?
It returns the same result if given the same arguments , If our function reads external files, it’s not a pure function — the file’s contents can change, Any function that relies on a random number generator cannot be pure, It does not cause any observable side effects
## What are the benefits of a pure function?
The code’s definitely easier to test
## What is immutability?
its state cannot change after it’s created
## What is Referential transparency?
Basically, if a function consistently yields the same result for the same input, it is referentially transparent.

pure functions + immutable data = referential transparency

### for more information checkout this source [Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)


# What is a module?

it is a component, function and variable that you intend to use in other applications

## What does the word ‘require’ do?

it would import the module into the application

## How do we bring another module into the file the we are working in?

we have to import it using **require**.

## What do we have to do to make a module available?

export it from its original path then import it to our application using require

### For more info checkout this source [Node JS Tutorial for Beginners #6 - Modules and require()](https://www.youtube.com/watch?v=xHLd36QoS4k)

## Things I want to know more about
- importing the modules
