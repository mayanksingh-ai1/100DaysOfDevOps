# Day 02 - Core Git Commands

## 📖 Kya seekha
- Git ke 3 main areas: **Working Directory → Staging Area → Repository (.git)**
- File ka lifecycle: Untracked → Staged → Committed
- Commit history dekhna aur samajhna

## 💻 Commands jo try kiye

### Staging & Committing
```bash
git status                    # kaunsi files modified/staged/untracked hain
git add file.txt                # ek file stage karta hai
git add .                         # saari changed files stage karta hai
git add *.md                        # sirf .md files stage karta hai
git commit -m "message"               # staged changes ko commit karta hai
git commit -am "message"                # tracked files ko add + commit ek saath (nayi files ke liye kaam nahi karta)
```

### History dekhna
```bash
git log                       # poori commit history
git log --oneline               # short format mein history
git log --oneline --graph         # branch structure ke saath
git show <commit-hash>              # ek specific commit ke changes dikhata hai
git diff                              # unstaged changes dikhata hai
git diff --staged                       # staged changes dikhata hai
```

### Undo karna
```bash
git restore file.txt          # working directory ke changes undo karta hai
git restore --staged file.txt   # staging se hata deta hai (unstage)
git reset --soft HEAD~1           # last commit undo karta hai (changes staged rehte hain)
git reset --hard HEAD~1             # last commit + changes dono delete (careful!)
```

## 🎯 Challenge jo face kiya
- `git reset --hard` samajhne mein dar laga kyunki ye permanently changes delete kar deta hai — practice karte waqt ek test repo use kiya safety ke liye

## 📝 Key Takeaways
- Staging area ek "draft zone" hai — commit se pehle review karne ka mauka deta hai
- Commit messages clear aur meaningful hone chahiye (e.g. "Fix login bug" na ki "update")
- `git log --oneline` daily use ke liye sabse handy command hai

## 🔜 Kal kya seekhunga
- Branching aur merging — parallel development kaise hoti hai

---
*Day 2 of #100DaysOfDevOps*
