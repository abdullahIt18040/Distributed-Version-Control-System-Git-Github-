# `git push --set-upstream origin feature`

> **সঠিক কমান্ড:**

```bash
git push --set-upstream origin feature
```

অথবা সংক্ষেপে:

```bash
git push -u origin feature
```

## ব্যাখ্যা

* `git push` → Local branch Remote repository-তে Push করে।
* `--set-upstream` (বা `-u`) → Local branch-এর সাথে Remote branch-এর **tracking (upstream) relationship** তৈরি করে।
* `origin` → Remote repository-এর নাম।
* `feature` → Push করার Local branch-এর নাম।

---

## উদাহরণ

প্রথমবার `feature` branch Push করছেন:

```bash
git checkout -b feature
git add .
git commit -m "Add login feature"
git push -u origin feature
```

এখন Git মনে রাখবে:

```text
Local branch:   feature
        │
        ▼
Remote branch:  origin/feature
```

---

## এরপর কী সুবিধা?

প্রথমবার `-u` ব্যবহার করার পর, পরবর্তীতে শুধু লিখলেই হবে:

```bash
git push
```

এবং

```bash
git pull
```

বারবার `origin feature` লিখতে হবে না, কারণ Git জানে `feature` branch, `origin/feature`-কে track করছে।

---

## যদি `-u` ব্যবহার না করেন

প্রতিবার লিখতে হবে:

```bash
git push origin feature
git pull origin feature
```

---

## মনে রাখুন

* **`-u` = `--set-upstream`**
* **প্রথমবার Branch Push করার সময় ব্যবহার করা হয়।**
* **এটি Local branch-এর সাথে Remote branch-এর tracking relationship তৈরি করে।**

  # Merge Conflict

## Merge Conflict কী?

**Merge Conflict** ঘটে যখন দুটি Branch-এর **একই File-এর একই লাইনে** ভিন্ন পরিবর্তন করা হয় এবং Git বুঝতে পারে না কোন পরিবর্তনটি রাখবে।

---

## উদাহরণ

### `main` Branch

```java
public String getName() {
    return "Mamun";
}
```

### `feature` Branch

```java
public String getName() {
    return "Abdullah";
}
```

এখন `feature` branch-কে `main`-এ Merge করলে:

```bash
git checkout main
git merge feature
```

Git Conflict দেখাবে:

```text
Auto-merging UserService.java
CONFLICT (content): Merge conflict in UserService.java
Automatic merge failed; fix conflicts and then commit the result.
```

---

## Conflict File

Git File-এ নিচের Marker যোগ করবে:

```java
<<<<<<< HEAD
return "Mamun";
=======
return "Abdullah";
>>>>>>> feature
```

* `<<<<<<< HEAD` → বর্তমান Branch (`main`)
* `=======` → দুই Version-এর বিভাজক
* `>>>>>>> feature` → Merge হওয়া Branch (`feature`)

---

## Merge Conflict সমাধান

1. File খুলে সঠিক Code নির্বাচন বা Combine করুন।

```java
return "Abdullah";
```

অথবা

```java
return "Mamun Abdullah";
```

2. Conflict Marker (`<<<<<<<`, `=======`, `>>>>>>>`) মুছে ফেলুন।
3. File Save করুন।

তারপর:

```bash
git add .
git commit
```

Merge সম্পন্ন হবে।

---

## Merge Conflict এড়ানোর উপায়

* নিয়মিত `git pull` করুন।
* ছোট ছোট Commit করুন।
* একই File-এর একই অংশে একাধিক Developer একসাথে পরিবর্তন করা এড়িয়ে চলুন।
* Feature Branch-কে নিয়মিত `main`-এর সাথে Sync রাখুন।

---

## মনে রাখুন

> **Merge Conflict = একই File-এর একই লাইনে দুই Branch-এর ভিন্ন পরিবর্তন হলে Git সিদ্ধান্ত নিতে না পারার অবস্থা।**

