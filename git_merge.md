# Git Merge – Short Note

## `git merge` কী?

`git merge` দুটি Branch-এর changes **একত্রে (combine)** করে। প্রয়োজনে একটি **Merge Commit** তৈরি হয় এবং উভয় Branch-এর history সংরক্ষিত থাকে।

---

## Syntax

```bash
git merge <branch-name>
```

---

## উদাহরণ

ধরুন `feature` branch-এর কাজ `main`-এ যুক্ত করতে চান।

```bash
git checkout main
git merge feature
```

---

## Merge-এর আগে

```text
main:    A --- B --- C

feature:       \
                D --- E
```

---

## Merge-এর পরে

```text
A --- B --- C -------- M   (main)
      \              /
       D ---------- E      (feature)
```

* **`M` = Merge Commit**
* `feature` branch-এর সব changes `main` branch-এ যুক্ত হয়েছে।
* দুই Branch-এর history সংরক্ষিত থাকে।

---

## Merge Commit কী?

Merge Commit হলো একটি **বিশেষ Commit**, যা দুটি Branch-এর history-কে একত্রে যুক্ত করে। এটি দেখায় যে `feature` branch-এর changes `main` branch-এ Merge হয়েছে।

---

## সুবিধা

* Branch history সংরক্ষিত থাকে।
* Team collaboration-এর জন্য নিরাপদ।
* Shared/Public Branch-এর জন্য Recommended।

---

## কখন `git merge` ব্যবহার করবেন?

* Feature Branch → `main` Merge করার সময়।
* Team Project-এ Shared/Public Branch-এর জন্য।
* যখন Branch History সংরক্ষণ করতে চান।

---

## মনে রাখুন

* **Git Merge = Branch Combine + Merge Commit + History Preserve**
* **Git Rebase = Commit Move + No Merge Commit + Clean Linear History**
