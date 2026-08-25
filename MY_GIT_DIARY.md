# 📓 Meri Git & GitHub Ki Personal Diary (Revision Notes)

---

## 📍 Step 1: Initialization & Identity Setup
* `git config --global user.name "Harsh"` ➔ Git ko apna naam batana.
* `git config --global user.email "harsh@example.com"` ➔ Git ko apna email batana.
* `git init` ➔ Kisi folder ko Git repository banana (hidden `.git` folder banta hai).

---

## 📍 Step 2: First Commit & Inspection
* `git status` ➔ Halat check karna (Red = Untracked/Modified, Green = Staged ready to commit).
* `git add <file>` ➔ Kisi specific file ko Staging Area (packing box) mein daalna.
* `git commit -m "feat: message"` ➔ Staged files ka permanent snapshot lena.
* `git log --oneline` ➔ Ab tak ke saare commits ki 1-line list dekhna.

---

## 📍 Step 3: Modifying Files, Staging All & `git diff`
* `git diff` ➔ Working directory ke unstaged badlav dekhna (Red = Deleted lines, Green = Added lines).
* `git add .` ➔ Saari nayi aur modified files ko ek sath stage karna.
* `git diff --staged` ➔ Staging area mein jo pack kiya hai uska diff dekhna.

---

## 📍 Step 4: Branching (Feature Isolation)
* `git branch` ➔ Saari local branches ki list dekhna (* active branch ke aage hota hai).
* `git switch -c <branch-name>` ➔ Nayi branch banana AUR turant uspe jump (switch) karna.
* `git switch <branch-name>` ➔ Kisi existing branch par switch karna.
* `git log --oneline --graph --all` ➔ Saari branches ka visual commit tree dekhna.

---

## 📍 Step 5: Merging & Cleaning Up Branches
* `git merge <branch-name>` ➔ Dusri branch ke code ko apni current branch mein milana.
* `git branch -d <branch-name>` ➔ Merge ho chuki feature branch ko safely delete karna.

---

## 📍 Step 6: Remote Repositories & GitHub Collaboration
* `git remote add origin <URL>` ➔ Apne local project ko GitHub ke online repo se jorna ('origin' nickname hota hai).
* `git remote -v` ➔ Check karna kaunsa remote link connected hai.
* `git push -u origin master` ➔ Local commits ko GitHub par upload karna (`-u` upstream permanently set karta hai).
* `git push` ➔ Upstream set hone ke baad simple code upload karna.
* `git pull origin master` ➔ GitHub se team ke naye commits download karke seedha merge karna.
* `git fetch origin` ➔ GitHub se updates check/download karna bina local code ko disturb kiye.
