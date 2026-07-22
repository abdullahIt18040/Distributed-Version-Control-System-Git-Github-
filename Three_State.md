## Git Three States (Three Areas)
```
Git মূলত File-কে তিনটি State বা Area-তে রাখে:

Working Directory
        ↓ git add
Staging Area
        ↓ git commit
Local Repository
```
## Complete Git Three State Flow
```
             Edit Code
                |
                ↓
       +----------------+
       | Working        |
       | Directory      |
       +----------------+
                |
             git add
                |
                ↓
       +----------------+
       | Staging Area   |
       +----------------+
                |
          git commit
                |
                ↓
       +----------------+
       | Local          |
       | Repository     |
       +----------------+
                |
            git push
                |
                ↓
       +----------------+
       | Remote Repo    |
       | (GitHub)       |
       +----------------+
```
## What is git status?
```
git status হলো একটি Git command যা আমাদের Project-এর বর্তমান অবস্থা (Current State) দেখায়।

এটি দেখায়:

কোন File modified হয়েছে
কোন File new/untracked
কোন File staged হয়েছে
কোন File commit করার জন্য ready
কোন Branch-এ আমরা আছি
```
