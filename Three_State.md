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
### What is git log?
```

git log হলো একটি Git command যা Repository-এর Commit History দেখায়।

এটি দেখায়:

কে Commit করেছে (Author)
কখন Commit করেছে (Date)
Commit Message
Commit ID (Hash)
Command
git log

Example Output:

commit a8f5c92d8e1b
Author: Abdullah
Date: Wed Jul 22 2026

    Added login API


commit b72a9c4f12ab
Author: Rahim
Date: Tue Jul 21 2026

    Created user module
Commit ID কী?

প্রতিটি Commit-এর একটি unique ID থাকে।

Example:

a8f5c92d8e1b

এটি ব্যবহার করে নির্দিষ্ট Commit খুঁজে বের করা যায়।

Short Log

বেশি Detail না দেখে শুধু Summary দেখতে:

git log --oneline

Output:

a8f5c92 Added login API
b72a9c4 Created user module
c31d8e1 Initial commit
Graph View

Branch এবং Merge দেখতে:

git log --graph --oneline

Example:

* a8f5c92 Added login API
|\
| * b72a9c4 Payment feature
|/
* c31d8e1 Initial commit
Specific Author-এর Commit
git log --author="Abdullah"
Last N Commit দেখানো

Example: Last 5 Commit

git log -5
Commit Details দেখা
git show commit-id

Example:

git show a8f5c92

এটি দেখাবে:

কোন File Change হয়েছে
কী Code Add/Remove হয়েছে
Commit Details দেখা
git show commit-id

Example:

git show a8f5c92

এটি দেখাবে:

কোন File Change হয়েছে
কী Code Add/Remove হয়েছে


git status → বর্তমান অবস্থা দেখায়

git log → পুরোনো পরিবর্তনের ইতিহাস দেখায়.

``` 
