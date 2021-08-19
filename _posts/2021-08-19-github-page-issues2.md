---
layout: post
title: 깃헙페이지 with jekyll-theme-yat 생성시 이슈들, 해결방법 2
categories: markdown
tags: [깃헙페이지, 깃헙 엑션]
---

Short summary after trouble shooting
- `build-jekyll.yml` for github action can be updated so I needed to update it

## Issue. Unable to build GitHub page
- What happened: All of sudden, the github action pipeline broke during building
- Why?: build-jekyll.yml at [github action repo](https://github.com/jeffreytse/jekyll-deploy-action) has been changed 
- How I know: I reported the error and I got a [reply](https://github.com/jeffreytse/jekyll-theme-yat/issues/57)
- How to solve?: 
    - I updated my `build-jekyll.yml`
    - [The commit I made ](https://github.com/dalpengholic/small_logs/commit/649e9274eb7b0ff15534fbac8fb6cce55c71d2c1)

