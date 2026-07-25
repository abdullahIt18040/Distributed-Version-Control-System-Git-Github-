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
