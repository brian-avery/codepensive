---
layout:     post 
title:      "Why Simple Programs are Important"
date:       2017-10-08
author:     "Brian Avery"
URL: "/2017/10/08/why-simple-programs-are-important/"
image:      "https://img.zhaohuabing.com/post-bg-2015.jpg"
categories:  ["Clean Programming" ]
---
In his talk <a href="https://www.youtube.com/watch?v=rFejpH_tAHM">Simplicity is Complicated </a>from dotGo 2015, Rob Pike states that readable code is reliable code; it's easier to understand, easier to work on, and easier to fix when it breaks.

As programmers, our job is to take complicated problems and design solutions for them using computers.  We write these solutions for two audiences. Humans, and computers. The computers require explicit language telling them each step of what they are supposed to do, something that programmers can get very good at, but is still not their native way of thinking. The best solution to this is to find a happy medium somewhere between the two. A good program should be easily readable and obvious in its behavior, while addressing all of the details for the computer to execute the program.

A good program should read like a good story. This is why I love the Go programming language. The language abstracts away the lower level complexity so that the programmer can focus on the problem at hand. Memory management, implementation of low level APIs, and much of the other complexity that a language such as C or C++ requires is all implemented out of the box.

A programmer may be able to develop a more optimized solution by hand coding a solution for this specific problem, but this usually comes at the expense of complexity in the software. This complexity often leads to a program that is harder to debug and takes more work for any developer to come up to speed with the software at a later date. Also, modern programming languages and compilers usually have highly optimized, efficient solutions out of the box, so the trade off in complexity vs a higher level language is most likely not often worth it.

Abstracting away the complexity means that a programmer can focus on implementing a solution to the problem at hand rather than the low level system management. In exchange, you can get a program that is much easier to read, telling you how it's solving the problem rather than how it is managing resources. This focus on the problem itself makes the solution easier to understand, logic issues easier to find, and often makes it easier for another programmer to come in and figure out what's going on.