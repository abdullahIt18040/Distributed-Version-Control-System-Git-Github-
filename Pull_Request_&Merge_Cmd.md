## Pull Request (PR)
```
Pull Request (PR) হলো GitHub-এর একটি Feature, যার মাধ্যমে নিজের Branch-এর পরিবর্তন (changes) অন্য Branch-এ (যেমন main) Merge করার জন্য Review ও Approval চাওয়া হয়।

কেন ব্যবহার করা হয়?
কোড Review করার জন্য।
Team Collaboration সহজ করতে।
Bug বা ভুল Merge হওয়া কমাতে।
Approval পাওয়ার পর Code Merge করতে।
Pull Request Flow
নতুন Branch তৈরি করুন।
Code পরিবর্তন করুন।
Commit করুন।
Remote-এ Push করুন।
GitHub-এ Create Pull Request করুন।
Team Lead/Reviewer Code Review করবেন।
Approval হলে Branch main-এ Merge হবে।
উদাহরণ
git checkout -b feature/login
git add .
git commit -m "Add login feature"
git push -u origin feature/login

তারপর GitHub-এ গিয়ে Compare & Pull Request ক্লিক করে PR তৈরি করুন।

সহজভাবে মনে রাখুন:
Pull Request = "আমার Code Review করে main Branch-এ Merge করার অনুমতি দিন।"
```
