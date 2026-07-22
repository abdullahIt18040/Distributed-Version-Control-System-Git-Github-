## Repository (Repo)
```
যখন আমরা কোনো Project Folder-কে Git দিয়ে Track করা শুরু করি, তখন সেই Folder একটি Git Repository হয়ে যায়।
A Repository (Repo) হলো এমন একটি folder ,which track by git .
 যেখানে একটি Project-এর Source Code, Files, এবং Git History (Commits, Branches, Tags) সংরক্ষণ করা হয়।
এটি করার জন্য:

git init

Command ব্যবহার করা হয়।

git init চালানোর পরে Project Folder-এর ভিতরে একটি hidden folder তৈরি হয়:

Project Folder

│── src/
│── pom.xml
│── README.md
│── .git/

.git folder-এর মধ্যে Git সংরক্ষণ করে:

Commit History
Branch Information
Configuration
Object Data

তখন এই Project Folder-কে বলা হয়:

Local Git Repository
```

## Local Repository vs Remote Repository
```
Local Repository: আপনার নিজের Computer-এ থাকে।
Remote Repository: GitHub, GitLab বা Bitbucket-এর মতো Online Server-এ থাকে, যা Team-এর সবাই Access করতে পারে।
```
## git Clone
## What is Git Clone?
```
Git Clone হলো GitHub বা অন্য কোনো Remote Repository থেকে একটি সম্পূর্ণ Project Copy করে নিজের Local Computer-এ আনার process।

অর্থাৎ:

Remote Repository (GitHub) → Local Repository (Your Computer)

Clone Command
git clone <repository-url>
Example:
git clone https://github.com/company/employee-management.git
```
