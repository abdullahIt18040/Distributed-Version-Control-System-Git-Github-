# Git Rebase – Short Note

## `git rebase` কী?

`git rebase` একটি Branch-এর commit-গুলোকে অন্য Branch-এর **সর্বশেষ commit (new base)**-এর উপর পুনরায় বসায় (reapply)। এর ফলে **history linear ও পরিষ্কার** থাকে এবং **Merge Commit তৈরি হয় না**।

### Syntax

```bash
git rebase <branch-name>
```

### উদাহরণ

```bash
git checkout feature
git rebase main
```

**অর্থ:** `feature` branch-এর commit-গুলো `main` branch-এর সর্বশেষ commit-এর উপর পুনরায় প্রয়োগ হবে।

### সুবিধা

* Clean & Linear commit history
* Merge Commit তৈরি হয় না
* Feature branch সহজে update করা যায়

### কখন ব্যবহার করবেন?

* Local Feature Branch update করতে
* Pull Request করার আগে history পরিষ্কার রাখতে

### কখন ব্যবহার করবেন না?

* Shared/Public branch (`main`, `develop`) এ **rebase করবেন না**।
* কারণ Rebase commit history পরিবর্তন করে।

### Golden Rule

> **Never Rebase a Shared/Public Branch. Use Rebase only on your Local Feature Branch.**
