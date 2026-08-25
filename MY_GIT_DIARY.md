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

---

## 📍 Step 8: Ignoring Secrets & Heavy Files (`.gitignore`)
* `.gitignore` ➔ Aisi text file jisme mention kiye gaye files/folders ko Git completely ignore kar deta hai.
* `secret.env` ➔ Kisi specific secret password file ko ignore karna.
* `*.log` ➔ Saari log files ko ignore karna.
* `node_modules/` ➔ Heavy libraries/packages folder ko ignore karna.
* *Note:* Terminal par `(END)` se bahar nikalne ke liye `q` dabate hain.

---

## 📍 Step 9: Undoing Mistakes & Staging Fixes
* `git restore <file>` ➔ Unstaged badlaav ko mita kar file ko pichle commit wali sahi condition mein wapas laana.
* `git restore --staged <file>` ➔ Staging area (box) se file ko bahar nikalna bina code delete kiye.
* `git commit --amend -m "new message"` ➔ Last commit ke message ko modify/replace karna (clean commit history ke liye).

---

## 📍 Step 10: Temporary Code Locker (`git stash`)
* `git stash` ➔ Adhoore/uncommitted code ko temporary secret locker mein daal kar working area clean karna.
* `git stash pop` ➔ Locker se adhoora code wapas nikal kar file mein paste karna aur locker khali karna.
* `git stash list` ➔ Locker mein pade saare stashes ki list dekhna.

---

## 📍 Step 11: Time Machine & Safe Rollback (`git revert` vs `git reset`)
* `git revert <commit-hash>` ya `HEAD` ➔ Galti wale commit ko safely undo karna (naya reverse commit banta hai, history delete nahi hoti - 100% safe for GitHub).
* `git reset --soft HEAD~1` ➔ Last commit ko undo karna lekin code ko Staging Area mein bacha ke rakhna.
* `git reset --hard HEAD~1` ➔ Last commit aur code dono ko poori tarah mita dena (⚠️ Khatarnak).

---

## 📍 Step 12: Productivity Shortcuts (`git aliases`)
* `git config --global alias.st status` ➔ `git st` se status dekhna.
* `git config --global alias.cm "commit -m"` ➔ `git cm "msg"` se commit karna.
* `git config --global alias.br branch` ➔ `git br` se branch dekhna.
* `git config --global alias.hist "log --oneline --graph --all"` ➔ `git hist` se visual tree graph dekhna.

---

## 📍 Step 13: Milestone Releases (`git tags`)
* `git tag -a v1.0.0 -m "Release message"` ➔ Kisi milestone commit par official version tag lagana.
* `git tag` ➔ Saare version tags ki list dekhna.
* `git push origin --tags` ➔ Saare tags ko GitHub Releases par upload karna.

---

## 📍 Step 14: Open-Source Contribution Workflow (`Fork ➔ Clone ➔ PR`)
1. **Fork:** Kisi dusre ki repository ke top-right par *Fork* button dabakar uski ek copy apne GitHub account mein save karna.
2. **Clone:** Apni forked repo ko computer par download karna: `git clone <forked-url>`.
3. **Branch & Code:** Nayi branch banana (`git switch -c fix-bug`), code fix karke commit karna.
4. **Push:** Apni forked repo par push karna: `git push -u origin fix-bug`.
5. **Open PR:** Original project owner ko *Pull Request* bhejna taaki woh aapka code accept kar sakein.
