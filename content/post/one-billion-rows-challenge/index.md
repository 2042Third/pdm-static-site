---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "One Billion Rows Challenge"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2024-06-21T00:00:00Z
lastmod: 2024-06-21T00:00:00Z
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
# Single Threaded One Billion Rows Challenge

This is a solution to the [one billion rows challenge](https://github.com/gunnarmorling/1brc) using a single thread in C++.
Not optimized at all, but still faster than most multi-threaded solutions.
[Code in my Github Repo](https://github.com/2042Third/1br-challenge)

## Results
| Hardware | Time (seconds) |
|----------|----------------|
| Apple M2 | 0.55           |

## Reason to Not Use Multi-threading
This is only a 12 Gb file, and the calculation is extremely simple (two comparisons and one addition each iteration).
Thus, the bottleneck is going to be the IO operation of reading the file. In fact,
using multi-threading will make it slower due to the added overhead of context switching.

## Methods
- From my experience, reading binary files (both signle and multi-threaded) using memory mapped files is the best, especially when the file is large.
  - I used my encryption memory mapping class to read the file.
- The cost of a IO heavy operation like reading a file is mostly from actually accessing the memory mapped pointer to the file. Thus, it is best to minimize
  the number of times the pointer is accessed. In this case, each character only need to be accessed once from the memory mapped pointer.
- The map that keeps track of the statistics of each city can just use `std::string` since it didn't give me much of a performance improvement when
  I used custom comparator and equality checker with `char*`.
- The map or specifically `std::unordered_map` should be used since the challenge said there will be at most 10,000 cities.
  Using `std::unordered_map` allows us to call `std::unordered_map::reserve(int)` to make inserts O(1) instead of O(log n).


