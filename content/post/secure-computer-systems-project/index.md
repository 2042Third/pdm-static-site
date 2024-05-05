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

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
## Secure Computer Systems Final Project
### The Worse Case Scenario Prime+Probe Attack
The highlighted columns are the sets each vault is running on. 
![output1.png](..%2F..%2F..%2Fstatic%2Fstaticfiles%2Fscs-final%2Foutput1.png "1 vault running on 1 core.")
![output2.png](..%2F..%2F..%2Fstatic%2Fstaticfiles%2Fscs-final%2Foutput2.png "2 vaults running on 1 core.")
![output3.png](..%2F..%2F..%2Fstatic%2Fstaticfiles%2Fscs-final%2Foutput3.png "3 vaults running on 1 core.")
![output4.png](..%2F..%2F..%2Fstatic%2Fstaticfiles%2Fscs-final%2Foutput4.png "4 vaults running on 1 core.")
![output5.png](..%2F..%2F..%2Fstatic%2Fstaticfiles%2Fscs-final%2Foutput5.png "5 vaults running on 1 core.")
![output6.png](..%2F..%2F..%2Fstatic%2Fstaticfiles%2Fscs-final%2Foutput6.png "6 vaults running on 1 core.")
![output7.png](..%2F..%2F..%2Fstatic%2Fstaticfiles%2Fscs-final%2Foutput7.png "7 vaults running on 1 core.")
![output8.png](..%2F..%2F..%2Fstatic%2Fstaticfiles%2Fscs-final%2Foutput8.png "8 vaults running on 1 core.")
![output9.png](..%2F..%2F..%2Fstatic%2Fstaticfiles%2Fscs-final%2Foutput9.png "9 vaults running on 1 core.")
![output10.png](..%2F..%2F..%2Fstatic%2Fstaticfiles%2Fscs-final%2Foutput10.png "10 vaults running on 1 core.")

### Performance of Multi-Threaded Encryption Program (ChaCha20) Using This Protection Mechanism
Due to the nature of the ChaCha20 algorithm, it is able to encrypt on arbitrary number of threads. 
I implemented and made all the encryption algorithm used in this command line program, and it also used in multiple 
different projects for the encryption and decryption of data, including QT6, Angular(WebAssembly), React Native(iOS and Android binary).   

The expectation is that using the protection method described above, the performance of the encryption program will *not* 
be affected than the single thread performance. 

The multi-threading mechanism is rewritten to be able to run all threads on a chosen physical core *on Linux*. 
This graph below is the performance of the encryption program running on 1 to 30 threads of both normal multi-threading 
and all threads on the same core. 

![enc_output.png](..%2F..%2F..%2Fstatic%2Fstaticfiles%2Fscs-final%2Fenc_output.png)
