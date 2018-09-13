---
title: GIT常用命令
tags:
  - Testing
categories: GIT
---
### 版本回退后强制推送远程分支
git reset - -hard HEAD~
git push origin HEAD - -force

### 未push时撤销commit
git reset - -hard commit_id  完成撤销，同时将代码恢复到commit_id对应的版本
git reset commit_id         完成撤销，不对代码进行撤销