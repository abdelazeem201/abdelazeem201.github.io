---
title: 'Static timing analysis'
date: 2022-07-23
permalink: /posts/2022/07/blog-post-3/
tags:
  - ASIC Design
  - PnR
  - STA
---

Problem:
========
# *The Ultimate Guide to Static Timing Analysis*

Solution:
=========

Life would be simpler for a lot of engineers if their designs met their timing requirements
the first time around. Unfortunately, it is not as simple as that. Time and effort spent to
meet timing is increasing to unheard of levels. Designers resort to constraining their
synthesis and place & route tools to achieve the required performance. However,
generating the proper constraints is a hit-and-miss game for designers, while verifying
them becomes someone else’s nightmare.

Designers typically load the implementation tools with the design constraints and hope the
tools give the results they need, i.e. zero timing violations. However in most cases after first
pass the timing reports give 100s to 1000s of violations. When diving into the timing report
looking at specific paths, they ask the question: Is it a real path that can occur? Static
timing engines in the synthesis and P&R tools just trace through all paths in the design to
find the longest path. They do not evaluate to see if the path can functionally occur. If the
implementation tool can meet the timing, designers do not worry about this question. But
if they can know which critical timing paths are false they could be eliminated from the
timing report or, even better, eliminated from the optimization run. If the optimization tool
has fewer paths to work on, the better chance it has in meeting timing on other critical
paths.
