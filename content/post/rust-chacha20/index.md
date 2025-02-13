---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Rust PDM Encryption Rewrite"
subtitle: ""
summary: ""
authors: ["Yi Yang"]
tags: ["personal", "update", "pdm"]
categories: []
date: 2025-02-12T08:00:00Z
lastmod: 2025-02-12T08:00:00Z
featured: false
draft: false
editable: false
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

I rewrote one of my c++ chacha20 implementations in rust today. Writing only the single-threaded core encryption parts took only one day without too much optimization. 
But I feel like rust doesn't bring me the joy i get from writing c++ or golang. Not in terms of ergonomics, but the fact that I can't really just build a binary and use it everywhere. 

Using cargo is great, but cmake (despite how confusing it is), feels a lot more hands on, and I know exactly what I am going to get. Because I need to link to multiple platforms and binaries of all shapes and sizes (wasm, android, ios, windows, linux, macos) arm or x86, rust sounded so good. But looking deeper, it seems like I have to write c headers for the rust libraries. 

One important problem with Rust is interop with golang. Not that it can't do it, but C++ does it better, and "natively" builds to a dynamic library without a lot of setup on all platforms.

Not having care about memory management is ok. It just feels like I am writing Java but more organized. The borrow checker though is an interesting mechanism. I prepared for a few days reading a book on [Rust for Systems Programmers ](https://github.com/nrc/r4cppp/blob/master/README.md) and [Migrate from C to Rust](https://vnduongthanhtung.gitbooks.io/migrate-from-c-to-rust/content/string-manipulations.html), which I would recommend to read in addition to the official docs. 
These books helped me a lot with how the borrow checker works and what you can get away with with the C++ knowledge. I did have to beg the borrow check for an hour for an test case to work and later found out it wasn't even the borrow checker's problem... 

The Rust's ecosystem is well integrated. The cargo system feels like I am using golang or javascript. But it is weird that a systems language builds to a massive size with so little things inside and only two dependencies. 
Rust doesn't use the system's libc, which is pre-installed on all systems and even WASM has its own standard library that c/c++ can use to run in. Since Rust doesn't and can't just link to other Rust dynamically linked libraries, it has to build everything from scratch everytime (if I want to have no "unsafe" block). 

I will continue to try and learn more about Rust, but I think I will stick with C++ and Go for now for product projects.
