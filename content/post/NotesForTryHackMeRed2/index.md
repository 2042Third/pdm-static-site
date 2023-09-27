---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Notes For Try Hack Me Red 2"
subtitle: "Just some notes for myself"
summary: ""
authors: []
tags: []
categories: []
date: 2023-09-26T19:34:01-04:00
lastmod: 2023-09-26T19:34:01-04:00
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
### Rules of Engagement

It is a legally binding outline of the client's objective and scope. NDAs can also be used.
{{<rules-of-engagement-table >}}

**Engagement Planning**

**Engagement Plan :**

A overarching description of the technical requirements of the red team. Content can include: CONOPS, **Resource Plan**( timelines and information as a list: personnel, hardware, cloud requirements)

**Operations Plan:**

Specifics of the engagement, expanding the engagement plan. Contents can include: Operators, known info, responsibilities, Stopping Conditions, Technical Requirements

**Missions Plan:**

Exact commands to run and execution time of the engagement. Contents (required): Objectives, Operators, Exploits/Attacks, Targets (users/machines/objectives), Execution plan variations

**Remediation Plan:**

Describe what happens after the campaign. Contents: report, remediation consultation

**CONOPS (Concept of Operation)**

The CONOPS document is non-technical summary, assuming reader has zero technical background. However, should include details like common tooling, target group, etc. These include:

- Client name
- server provider
- timeframe
- General Objectives/Phases
- Other Training Objectives (Exfiltration)
- High-Level Tools/Techniques planned to be used
- Threat group to emulate (if any)
