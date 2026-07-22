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
