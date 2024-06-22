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
# Leetcode Notes

### 2507 - Smallest Value After Replacing With Sum of Prime Factors

```c++


class Solution {
public:
    int pf (int n) {
        int p = n;
        int out = 0;
        while (p % 2 == 0) { // 
            p /= 2;
            out += 2 ;
        }
        int sqt = sqrt(p);
        for (int i =3 ;i<=sqt ;i+=2) {
            while (p%i == 0) {
                p = p/i;
                out += i;
    
            }
        }
        if (p>2) {
            out = out+p;
        }
        return out;
    }

    int smallestValue(int n) {
        int p = n;
        while (1) {
            int a = pf (p) ;
            std::cout<< "Output: "<< a <<std::endl;
            if (a == p){
                return p;
            }
            else {
                p=a;
            }
        }
    }

    /**
    => 15 
    => 3 * 5 => 8
    => 2 * 2 * 2 => 6
    => 2 * 3 => 5 (is_prime ).
  
    */
};
```

#### Reason:

[Link to the math](https://www.geeksforgeeks.org/print-all-prime-factors-of-a-given-number/)

> Every composite number has at least one prime factor less than or equal to the square root of itself.
This property can be proved using a counter statement. Let a and b be two factors of n such that a*b = n. If both are greater than ?n, then a.b > ?n, * ?n, which contradicts the expression “a * b = n”.

