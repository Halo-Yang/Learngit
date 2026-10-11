---
description: This is the result of a test using branch
---

# Log:

1. created a calculator with 'plus' operation
2. added + commited it in master branch
3. created a branch feature/calculator                                --git switch -c feature/calculator
4. added minus operation in calculator.py, add + commit on branch feature/calculator
5. switch back to branch master

> **The calculator.py does not contain the minus operation!**

6. Combine the branch feature/calculator                              --git merge feature/calculator (in the master branch)

> **Minus operation is now in the calculator.py file on branch master**

7. created a branch feature/multiple
8. added multiple operation in calculator.py, add + commit on branch feature/multiple
9. switch back to branch master, and merge feature/multiple

> **Branch master & feature/multiple now contains the multiple operation**
> **Branch feature/calculator does not**

10. created a branch feature/add-one
11. added x + y + 1, add + commit on branch feature/add-one

12. created a branch feature/add-two
13. added x + y + 2, add + commit on branch feature/add-two

14. switch back to branch master, merge feature/add-one
15. merge feature/add-two

> **output:**  
    - print(f"x + y + 1 = {x + y + 1}")  
     -print(f"x + y + 2 = {x + y + 2}")  
    ++<<<<<<< HEAD  
    ++print(f"x + y + 1 = {x + y + 1}")  
    ++=======  
    ++print(f"x + y + 2 = {x + y + 2}")  
    ++>>>>>>> feature/add-two

> **Merge conflict**
> **Resolution: delete the conflict codes, and replace it with a code I like(such as add zero)**