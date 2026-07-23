## `git commit --amend`

```bash id="p9x7xk"
git commit --amend
```

**সংক্ষিপ্ত নোট:**

* আগের **last commit modify/update** করার জন্য ব্যবহার করা হয়।
* নতুন commit তৈরি না করে আগের commit-এর সাথে নতুন change যোগ করে।
* Commit message পরিবর্তন করতেও ব্যবহার করা যায়।

### Example:

প্রথমে commit:

```bash id="v0f4g4"
git commit -m "Add login feature"
```

কিছু ভুল হয়েছে, নতুন file যোগ করতে চান:

```bash id="j7s9i2"
git add .
git commit --amend
```

এখন আগের commit update হয়ে যাবে।

### Commit message change:

```bash id="m4v0n8"
git commit --amend -m "Updated login feature"
```

### সতর্কতা:

* Shared branch (`main`) এ push করা commit amend করলে সমস্যা হতে পারে।
* কারণ commit-এর history পরিবর্তন হয়ে যায়।
* Local commit-এর জন্য বেশি ব্যবহার করা হয়।

> **সহজভাবে মনে রাখুন:**
> `git commit --amend` = **Last commit edit/update করা।**
