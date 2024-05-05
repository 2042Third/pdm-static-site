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

[//]: # (![output1.png]&#40;/staticfiles/scs-final/output1.png "1 vault running on 1 core."&#41;)

[//]: # (![output2.png]&#40;/staticfiles/scs-final/output2.png "2 vaults running on 1 core."&#41;)

[//]: # (![output3.png]&#40;/staticfiles/scs-final/output3.png "3 vaults running on 1 core."&#41;)

[//]: # (![output4.png]&#40;/staticfiles/scs-final/output4.png "4 vaults running on 1 core."&#41;)

[//]: # (![output5.png]&#40;/staticfiles/scs-final/output5.png "5 vaults running on 1 core."&#41;)

[//]: # (![output6.png]&#40;/staticfiles/scs-final/output6.png "6 vaults running on 1 core."&#41;)

[//]: # (![output7.png]&#40;/staticfiles/scs-final/output7.png "7 vaults running on 1 core."&#41;)

[//]: # (![output8.png]&#40;/staticfiles/scs-final/output8.png "8 vaults running on 1 core."&#41;)

[//]: # (![output9.png]&#40;/staticfiles/scs-final/output9.png "9 vaults running on 1 core."&#41;)

[//]: # (![output10.png]&#40;/staticfiles/scs-final/output10.png "10 vaults running on 1 core."&#41;)

{{< gallery album="scs-final-pp" >}}


### Performance of Multi-Threaded Encryption Program (ChaCha20) Using This Protection Mechanism
Due to the nature of the ChaCha20 algorithm, it is able to encrypt on arbitrary number of threads. 
I implemented and made all the encryption algorithm used in this command line program, and it also used in multiple 
different projects for the encryption and decryption of data, including QT6, Angular(WebAssembly), React Native(iOS and Android binary).   

The expectation is that using the protection method described above, the performance of the encryption program will *not* 
be affected than the single thread performance. 

The multi-threading mechanism is rewritten to be able to run all threads on a chosen physical core *on Linux*. 
This graph below is the performance of the encryption program running on 1 to 30 threads of both normal multi-threading 
and all threads on the same core. 

![enc_output.png](/staticfiles/scs-final/enc_output.png)
