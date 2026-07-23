
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
