# Languages-Notes

Notes.

# Contents

1. [Ruby](#ruby)
1. [Ruby on Rails](#ruby-on-rails)
1. [Defintions](#definitions)

## Ruby

[Dynamic](#Static-vs-Dynamic-Typing), [interpreted](#Interpreted-vs-Compiled-Language), [reflective](#reflective-programming), object-oriented, general-purpose programming language.


## Ruby On Rails

#### Why use it

Ruby on Rails (ROL) is a web app development framework written in Ruby. It is opinionated on best practices for development so get on board if you're using this.

[ROL philosophy](https://guides.rubyonrails.org/getting_started.html)

> **Don't Repeat Yourself**: DRY is a principle of software development which states that
> *"Every piece of knowledge must have a single, unambiguous, authoritative representation within a system."* 
> By not writing the same information over and over again, our code is more maintainable, more extensible, and less buggy.
>
> **Convention Over Configuration**: Rails has opinions about the best way to do many things in a web application, and defaults 
> to this set of conventions, rather than require that you specify minutiae through endless configuration files.

## Definitions

Quick reference

1. [Interpreted vs Compiled-Language](Interpreted-vs-Compiled-Language)
1. [Static vs Dynamic Typing](Static-vs-Dynamic-Typing)

#### Interpreted vs Compiled Languages

Note: Technically, any language could be either of these. Typically a language is designated as "interpreted" or "compiled" by their canonical implementation being an Interpreter or a Compiler.

Just look at the wiki. [ref](https://en.wikipedia.org/wiki/Interpreter_(computing)#Compilers_versus_interpreters)

#### Static vs Dynamic Typing

```java
/* ex. Java */
String staticStr = "static typing";  // compiles fine
String invalidAttempt = 1;           // will fail at compilation
```

Python:
```python
# ex. Python

dynamicVar1 = "dynamic typing"  # is fine
dynamicVar2 = 1                 # is also fine

isStr1 = isinstance(dynamicVar1, str)  # returns true at runtime
isStr2 = isinstance(dynamicVar2, str)  # returns false at runtime
```

#### Reflective Programming

*"As a concrete definition, reflection is the ability of a computer program to examine and modify the structure and behavior (specifically the values, meta-data, properties and functions) of a program at runtime"*[ref](https://thesocietea.org/2016/02/programming-concepts-type-introspection-and-reflection/)
