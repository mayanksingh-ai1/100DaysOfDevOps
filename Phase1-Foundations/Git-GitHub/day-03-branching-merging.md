# Day 03 - Branching & Merging

## 📖 Kya seekha
- Branch kya hoti hai — ek independent line of development
- `main`/`master` branch usually production-ready code hoti hai
- Feature branches se without disturbing main code, naya kaam kar sakte hain
- Merge conflicts kab aate hain aur kaise resolve karte hain

## 💻 Commands jo try kiye

### Branch basics
```bash
git branch                        # saari local branches list karta hai
git branch feature-login             # nayi branch banata hai
git checkout feature-login              # branch switch karta hai
git checkout -b feature-signup            # naya branch banake switch bhi karta hai (shortcut)
git switch feature-login                    # naya (modern) tarika branch switch karne ka
git switch -c feature-payment                 # naya branch banake switch (modern)
git branch -d feature-login                     # branch delete karta hai (merged hone ke baad)
git branch -D feature-login                       # force delete (unmerged bhi)
```

### Merging
```bash
git checkout main
git merge feature-login          # feature-login ko main mein merge karta hai
```

### Conflict resolution
Jab do branches mein **same line** alag-alag change hoti hai, Git conflict dikhata hai:
```
<<<<<<< HEAD
your current branch ka code
=======
incoming branch ka code
>>>>>>> feature-login
```

Fix karne ka process:
1. File kholo, dono versions dekh ke decide karo kaunsa rakhna hai (ya dono combine karo)
2. `<<<<<<<`, `=======`, `>>>>>>>` markers delete karo
3. `git add <file>` karo
4. `git commit` karo (merge commit ban jayega)

## 🎯 Challenge jo face kiya
- Pehli baar merge conflict dekha, thoda confusing tha — samjha ki ye normal hai jab team saath kaam karti hai

## 📝 Key Takeaways
- Har naye feature/bug-fix ke liye alag branch banana best practice hai
- `main` branch ko directly edit nahi karna chahiye — hamesha branch banake PR se merge karna chahiye
- Conflicts darne wali cheez nahi — Git bas confirm karna chahta hai ki dono changes mein se sahi kaunsa hai

## 🔜 Kal kya seekhunga
- GitHub — remote repos, push/pull, pull requests

---
*Day 3 of #100DaysOfDevOps*
