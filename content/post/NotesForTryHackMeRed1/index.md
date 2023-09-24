---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Notes For Try Hack Me Red 1"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2023-09-24T19:34:01-04:00
lastmod: 2023-09-24T19:34:01-04:00
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
### Penetration Tests

Scan every host.

- **Exploit** the vulnerability.
- **Post-exploit**, extract info, pivot to gain more access to other hosts.

**Identify** and **Protect**, then see what impact an attacker has.

### Advanced Persistent Threats(APT), Regular pen not enough

Pen Tests are:

- loud
- doesn't include non-technical attack (social engineering)
- relaxation of security mechanics

APT: An advanced persistent threat (APT) is a stealthy threat actor, typically a nation state or state-sponsored group, which gains unauthorized access to a computer network and remains undetected for an extended period.

***

**Red team focus:**

- see defensive ream's capability of detecting and responding, instead of prevention.

**Red team** is a military term for a team that designs attacks to simulate the real attacks to attack **blue teams**.

In cybersecurity, red teams emulate black hats' **Tactics, Techniques and Procedures (TTPs).**

Red team, after defining clear goals (flags, or **crown jewels**), try to compromise the blue team's systems without being detected. Not all hosts are checked for vulnerability, because real attacks only need one.

Red teams' goals are not the flags, but to gain TTPs for the blue team to improve response or tweak control and detection capability.

**Red team improve on pen-tests in:**

- Find technical vulnerabilities with focus on stealth and evasion (**Tech. Infrastructure**)
- Use **social engineering** like phishing, phone calls, or social media to reveal information.
- Use **physical intrusion** like lock-picking, RFID cloning, exploiting electronic locks to access facilities.

Red Team exercise in multiple ways:

- **Fully simulating** the attacker's workflow
- **Assumed breached** targets
- **Table-top** with the blue team of theoretical attacks.

***

**Teams and functions of each in a red team engagement**

- Red Cell: offensive team, stimulating the target's strategic and tactical responses.
- Blue Cell: Mostly blue team members.
- White Cell: referee

**Red cell composition:**

- Red Team Lead: plan and organization at high-level
- Red Team Assistant Lead: Assisting, and assist writing engagement plans and documentation.
- Red Team Operator: Executes assignments delegated by team leads

*Just a typical composition not a guide.*

***

**Engagement Structure**

**Cyber Kill Chain** is used by red team to summarize and assess the steps and procedures of an engagement, and it's used by blue teams to map adversaries' behaviors.

**Lockheed Martin Cyber Kill Chain**:

1. Reconnaissance: email, Open Source Intelligence.
2. Weaponization: exploit with backdoor and deliverable payload
3. Delivery: via email, web, USB, etc.
4. Exploitation: MS17-010, Zero-Logon
5. Installation: Mimikatz, Rubeus
6. Command & Control (C2): Empire, Cobalt Strike
7. Actions on Objectives: Conti, LockBit2.0

***

**Other Useful Stuff**

Threat Intelligence Source: MITRE (https://attack.mitre.org/groups/G0008/)
