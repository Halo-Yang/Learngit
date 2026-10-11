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

- git reset --soft Head~1               撤销到 1 轮前的commit
- git reset --soft ORIG_HEAD            逆转 git reset --soft Head~1

- git stash                             临时保存当前未提交的修改
- git stash pop                         恢复最近一次stash，并在成功时删除

## Github
- git remote -v                         查看远程仓库
- git fetch origin                      获取远程更新，但不合并
- git pull                              获取远程更新，并且合并
- git push                              推到远程仓库
- git push -u origin feature-x          首次推送新分支并设置上游分支

## Branch
> check branch_test/result
- git branch feature-x                  创建分支，但不切换到分支
- git switch -c feature-x               创建分支，并切换到分支

- git branch                            查看本地分支
- git branch -a                         查看本地与远程跟踪分支
- git branch -vv                        查看分支与上游跟踪信息

- git switch master                     切换到master
- git switch -                          返回上一分支

- git merge feature-x                   将feature-x合与当前分支合并
- git branch -d feature-x               安全删除已合并的分支

## Worktree

- git worktree add -b ( branch ) ( path ) master        基于master创建新分支和worktree
- git worktree add ( path ) ( branch )                  在新目录里检出现有分支
- git worktree list                                     查看所有worktree

- git worktree remove ( path )                          移除一个worktree
- git worktree move ( old ) ( new )                     移动worktree

- git worktree prune                                    清理失效的worktree管理记录
- git worktree lock                                     防止worktree被移动/移除/清理