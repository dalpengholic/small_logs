---
layout: post
title: 깃헙페이지 with jekyll-theme-yat 생성시 이슈들, 해결방법
categories: markdown
tags: [깃헙페이지, 깃헙 엑션]
---

Short summary how to do troubleshootings
- Policies keep changing
- It is better to check the latest reference


## Issue1. Unable to see GitHub page when I first uploaded github page source code to gh-pages branch
- Why?: GitHub changed its policy that only 10? official themes are built automatically
- What I wanted: I did not want to build at my local laptop
- How to solve?: 
    - I decided to use github action provided [here](https://github.com/jeffreytse/jekyll-deploy-action)
    - When I upload source code to `master` branch, then github action starts automatically and it build and pushes artifacts to `gh-pages` branch 

## Issue2. Rendered page was wrong
- Why?: I did not manage `_config.yml` file
- How to solve? I edited `_config.yml` file 
