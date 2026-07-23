## `git pull`

```bash
git pull
```

**সংক্ষিপ্ত নোট:**

* Remote repository থেকে **সর্বশেষ (latest) changes** Local repository-তে নিয়ে আসে।
* এটি দুটি কাজ একসাথে করে:

  1. `git fetch` → Remote থেকে নতুন changes ডাউনলোড করে।
  2. `git merge` → সেই changes Local branch-এর সাথে Merge করে।
* `-u` দিয়ে upstream সেট করা থাকলে শুধু `git pull` লিখলেই হয়।

**উদাহরণ:**

```bash
git pull origin main
```

* `origin` = Remote repository
* `main` = যেখান থেকে changes আনবে

> **সহজভাবে মনে রাখুন:** `git pull` = **Remote → Local (Download + Merge)**.
