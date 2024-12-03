---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "From Java to Golang, what have I learned"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2024-12-03T00:00:00Z
lastmod: 2024-12-03T00:00:00Z
featured: false
draft: false
editable: false
math: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: [pdm]
---
# From Java to Golang, What Have I learned
From few years ago, Java has always been my go-to language for backend development. 
I have been using Java for developing logic applications, and even Android applications. 
However, I have always been curious about Golang and wanted to learn it. 
I have now completely rewritten my backend application in Golang.
In this article, I will share my experience and what I have learned from using Golang. 

## Syntax of Python, Safety of Java, Performance of C++
With a sound typing system, a language can statically infer the type of variable, and I think is helps a lot with the "ergonomics" of developing in it. 
This is something that even C++ can do, with the "auto" keyword, but not a lot of languages commit to it.
I think people are getting scared of messing around with typing in existing languages. For example, Typescript has a great intention of 
adding typing and the safety that comes from it into javascript, but it ended up being a mess to develop or maintain.
Even the "auto" keyword in C++ is controversial for hiding the type. 

Then the only way for a different typing system to be introduced, pain-free, is being a part of a new language.
Golang is a language that has a sound typing system, and it is statically typed, like the other "cool" new languages like Rust and Swift. 
All three of these are compiled languages. Swift being a platform-specific language, Rust being Rust, Golang sits in a comfortable position.
It is so easy to learn that it feels like it is like a universal binding to all the tools and interfaces that a backend would need, but in binary.
This is an important point for getting things done in the backend. 

## Garbage Collection: I Like It
It is nearly impossible to write a program without memory leaks in C++ or C on the first try (unless you use smart pointers, which comes with its own caveats), but Java and Golang achieve this by having a garbage collector.
It makes sense to have a garbage collector in a long-running program, like a server, because it is hard to predict when the memory will be freed or remapped.
Garbage collection cannot be added to C++ or languages that exposes pointers to the developer, which causes fragmentation without careful management.
You can control the fragmentation in C or C++ by manage reallocating structures and freeing them, but it is a pain to do so.
Golang exposes pointers, but you cannot do pointer arithmetic or cast an "uint64" to a "void*" and dereference it without making it a "unsafe" block.
And whenever memory gets remapped to a different location, the pointers are changed as well, so you cannot have a dangling pointer.
This is Go discouraging developers from handling pointers directly. 

## Stack Usage
Java has a stack for each thread, and the stack is used for storing local variables and function calls, and all the objects are stored in the heap.
C heavily uses the stack for storing local variables and function calls, and the heap is used for dynamically allocated memory.
Go also uses the stack for function calls and local variables, but its stack model is different from C or Java.
Go's stack is dynamically resizable. A goroutine starts with a small stack (e.g., 2 KB) that grows and shrinks as needed, unlike the fixed-size stack in C.
This design allows Go to use the stack more efficiently while supporting thousands of lightweight goroutines.
The Go GC (garbage collector) can scan the stack for pointers, which is not possible in C or C++. 
When objects escape the function scope, they are moved to the heap, similar to Java.
However, Go's compiler performs aggressive escape analysis to keep more objects on the stack when possible.

## Goroutines and Channels
Goroutines are lightweight thread-like entities that are managed by the Go runtime. This is extremely useful for a server, which needs to handle multiple connections concurrently.
In Java, you would need to create a new thread for each connection, which is expensive in terms of memory and CPU. I have made a websocket server in Java using different 
server technologies like Spring's Tomcat, Jetty, and Netty. All of them take more than 500 MB of memory just from the start. 
Then it has a fixed amount of memory usage for each additional websocket connection, I would be lucky to handle more than 50 connections without using the swap or crashing.
In Go however, I made a simple websocket server that starts 
with a memory usage of 7 MB, and even when handling 3000 websocket connections, it only uses 25 MB of memory, which is just preposterous.
I know there are ways to make Java more efficient, like using a thread pool and compiling in GraalVM, but it is not easy. 
For one GraalVM is not a drop-in replacement for the JVM, and it pretty much disables the dynamic features that Spring ecosystem relies on. 
And the thread pool is not as efficient or plug-and-play as goroutines. 

Channels are just amazing to use. It is like a thread-safe queue that can be used to communicate between goroutines and can act as a mutex.

## Conclusion: Golang is the Tool for the Job
Writing Golang doesn't feel like writing in a programming language, it feels like writing the tool or features themselves. 
It helps me decouple the logic from the language, and I can focus on the logic itself. I don't have think about memory management, because it efficient and never leaks.
I don't have to think about the threading model, because it is efficient and never crashes.
I don't have to think about the typing system, because it is sound and never fails.
I don't have to think about the performance, because it is fast and never slows down. I like it.
