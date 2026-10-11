---
description: This is the result of a test using worktree
---

# Log:

1. Initialized a branch master in student-manager
2. Wrote a main.py in student-manager, containing some student datas

3. Created a worktree with branch feature/average                               --git worktree feature/average ../student-average
4. Created a worktree with branch feature/ranking                               --git worktree feature/ranking ../student-ranking

> **Switch worktree by switching directories in bash**

5. Add calculate_average function in branch feature/average
6. Add rank_students function in branch feature/ranking

7. Switch back to student-manager/
8. Merge feature/average                                    --git merge feature/average
9. Merge feature/ranking                                    --git merge feature/ranking

> **Merge conflict**
> **resolve by accepting both changes (see branch_test)**

10. Delete worktree 1                                       --git worktree remove ../student-average
11. Delete worktree 2                                       --git worktree remove ../student-ranking
12. Delete branch 1                                         --git branch -d feature/average
13. Delete branch 2                                         --git branch -d feature/ranking