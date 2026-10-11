---
Description: This is a .md file listing some most important git commands
---

## Basics
- git init
- git clone ( url )
- git add file.py
- git add .
- git commit -m "message"
- git status
- git log

- git log --oneline                     简洁提交历史
- git log --oneline --graph --all       分支提交图

- git diff                              尚未暂存的修改
- git diff --staged                     已经暂存的修改

- git show HEAD                         最新提交内容

## 撤销 / 修复
- git restore file.py                   丢弃未暂存的修改
- git restore --staged file.py          将文件移出暂存区，保留工作区修改
- git commit --amend                    修改最近一次提交
- git revert ( commit )                 创建新提交，撤销指定提交的改动
- git stash                             临时保存当前未提交的修改
- git stash pop                         恢复最近一次stash，并在成功时删除

## Github
- git remote -v                         查看远程仓库
- git fetch origin                      获取远程更新，但不合并
- git pull                              获取远程更新，并且合并
- git push                              推到远程仓库
- git push -u origin feature-x          首次推送新分支并设置上游分支
