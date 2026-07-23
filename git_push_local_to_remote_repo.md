
## git remote add origin
```
git remote add origin https://github.com/abdullahIt18040/spring_lens.git

সংক্ষিপ্ত নোট:

Local repository-কে Remote (GitHub) repository-এর সাথে যুক্ত করে।
origin হলো Remote repository-এর alias (নাম)।
URL হলো GitHub repository-এর ঠিকানা।
এটি কোড Push করে না, শুধু Remote repository-এর ঠিকানা সেট করে।
এরপর git push origin main ব্যবহার করে কোড GitHub-এ পাঠানো যায়।
```
## git push -u --all origin
```
git push -u --all origin
git push -u  --all origin

সংক্ষিপ্ত নোট:

Local repository-এর সব branches origin remote-এ Push করে।
--all = সকল local branch।
origin = Remote repository-এর নাম (alias)।
এটি সব branch GitHub-এ আপলোড করে, শুধু main নয়।
```
cmd: 
## git push -u --all origin/ git push -u origin abdullah 
git push -u --all origin
```
-u (or --set-upstream) কেন ব্যবহার করা হয়?

Local branch-এর সাথে Remote branch-এর upstream (tracking) সম্পর্ক তৈরি করে।
এরপর থেকে শুধু git push বা git pull লিখলেই হবে; বারবার origin branch-name লিখতে হবে না।
অর্থাৎ, Git মনে রাখে কোন Remote branch-এর সাথে Local branch যুক্ত আছে।

উদাহরণ:

প্রথমবার:

git push -u origin main

পরবর্তীতে:

git push
git pull

কারণ main branch ইতোমধ্যেই origin/main-কে track করছে।
```
