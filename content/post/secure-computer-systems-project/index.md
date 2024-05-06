---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Secure Computer Systems Final Project"
subtitle: ""
summary: ""
authors: ["Yi Yang"]
tags: ["personal"]
categories: []
date: 2024-05-05T00:00:00Z
lastmod: 2024-05-05T08:00:00Z
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

gallery_item:
  - album: "scs-final-pp"
    image: "output1.png"
    caption: "1 vault running on 1 core."
  - album: "scs-final-pp"
    image: "output2.png"
    caption: "2 vaults running on 1 core."
  - album: "scs-final-pp"
    image: "output3.png"
    caption: "3 vaults running on 1 core."
  - album: "scs-final-pp"
    image: "output4.png"
    caption: "4 vaults running on 1 core."
  - album: "scs-final-pp"
    image: "output5.png"
    caption: "5 vaults running on 1 core."
  - album: "scs-final-pp"
    image: "output6.png"
    caption: "6 vaults running on 1 core."
  - album: "scs-final-pp"
    image: "output7.png"
    caption: "7 vaults running on 1 core."
  - album: "scs-final-pp"
    image: "output8.png"
    caption: "8 vaults running on 1 core."
  - album: "scs-final-pp"
    image: "output90.png"
    caption: "9 vaults running on 1 core."
  - album: "scs-final-pp"
    image: "output91.png"
    caption: "10 vaults running on 1 core."

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
## Secure Computer Systems Final Project

This project is to implement a protection mechanism against the Prime+Probe attack. There are two parts to this project. 
First is the show-case of attempted  Prime+Probe attack on a x86_64 Linux system with/without the protection in place. 
Second part is to implement this protection into a real-world production encryption library and see what the performance 
impact is.

The protection mechanism is to artificially increase the noise of a Spectre-type memory side-channel attack without 
compromising ANY functionality or performance. To do this, the program would first to be able to run on multiple threads.
If the program can multi-thread, then by running many threads on the same physical core, the noise of a Spectre attack would 
be dramatically increased, thus providing protection against Prime+Probe attack.

The next part is showing the worst case scenario of a Prime+Probe attack. And how this protection method can help.

### The Worse Case Scenario Prime+Probe Attack
The highlighted columns are the sets each vault is running on. 

{{< gallery album="scs-final-pp" >}}


### Performance of Multi-Threaded Encryption Program (ChaCha20) Using This Protection Mechanism
Due to the nature of the ChaCha20 algorithm, it is able to encrypt on arbitrary number of threads. 
I implemented the encryption algorithm used in this command line program; thus it is easier to implement this protection
 method.  

The expectation is that using the protection method described above, the performance of the encryption program will 
*not* be affected than the single thread performance. 

The multi-threading mechanism is rewritten to be able to run all threads on a chosen physical core *on Linux*. 
This graph below is the performance of the encryption program running on 1 to 30 threads of both normal 
multi-threading and all threads on the same core. 

![enc_output.png](/staticfiles/scs-final/enc_output.png)

![htop_screen_shot.jpg](/staticfiles/scs-final/htop_screen_shot.jpg)
