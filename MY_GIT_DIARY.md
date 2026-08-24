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
