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
>
> ## `git pull` – গুরুত্বপূর্ণ নোট

### ১. `git pull` করলে ভেতরে কী ঘটে?

`git pull` মূলত দুটি কাজ একসাথে করে:

```bash
git fetch
git merge
```

* **`git fetch`** → Remote repository থেকে সর্বশেষ changes Download করে।
* **`git merge`** → Download করা changes Local branch-এর সাথে Merge করে।

---

### ২. কখন `git pull` করবে?

* ✅ কাজ শুরু করার আগে (Latest code নেওয়ার জন্য)
* ✅ `git push` করার আগে (নিজের code up-to-date আছে কিনা নিশ্চিত করতে)

---

### ৩. `git pull` না করলে কী সমস্যা হতে পারে?

* Local code পুরনো (Outdated) হয়ে যাবে।
* `git push` করার সময় **Push Rejected** হতে পারে।
* Merge Conflict হওয়ার সম্ভাবনা বাড়ে।
* Team-এর সর্বশেষ changes মিস হয়ে যেতে পারে।

> **মনে রাখুন:** `git pull = git fetch + git merge`

