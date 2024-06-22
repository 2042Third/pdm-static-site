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
    int findAns(int n){
        int div=2,ans=0;
        while(n%2==0){
            ans+=2;
            n/=2;
        }
        int res=sqrt(n);
        for(int i=3;i<=res;i+=2){
            while(n%i==0){
                ans+=i;
                n/=i;
            }
        }
        if(n>2) ans+=n;
        return ans;
    }
    int smallestValue(int n) {
        while(1){
            int ans=findAns(n);
            if(ans==n) return n;
            n=ans;
        }
        return n;
    }
};
```

