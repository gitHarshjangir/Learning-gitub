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
* `git remote -v` ➔ Check karna kaunsa remote link (fetch/push) connected hai.
* `git push -u origin <branch>` ➔ Local commits ko GitHub par upload karna (`-u` upstream set karta hai, agli baar sirf `git push` chalega).
* `git fetch origin` ➔ GitHub se updates ki jaankari download karna bina local code ko chhede.
* `git pull origin <branch>` ➔ GitHub ke naye commits download karke seedha current branch mein merge karna (`fetch + merge`).
* `git clone <URL>` ➔ Kisi bhi public GitHub repo ka pura code aur history pehli baar apne computer par download karna.

---

## 📍 Step 7: Industry Feature-Branch & Pull Request (PR) Workflow
1. `git switch -c feature/<name>` ➔ Naye feature ke liye alag branch banana.
2. `git add .` & `git commit -m "feat: ..."` ➔ Feature ka commit lena.
3. `git push -u origin feature/<name>` ➔ Feature branch ko GitHub par upload karna.
4. **GitHub PR:** Website par *Compare & Pull Request* ➔ *Create PR* ➔ *Merge pull request* karna.
5. `git switch master` && `git pull origin master` ➔ Local master ko updated cloud code ke saath sync karna.
6. `git branch -d feature/<name>` ➔ Kaam hone ke baad purani feature branch ko delete karna.
