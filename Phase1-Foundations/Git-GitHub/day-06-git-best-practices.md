# Day 06 - Git Best Practices & Advanced Concepts

## 📖 Kya seekha
- `.gitignore` — kaunsi files Git track na kare
- Good commit message conventions
- Rebase vs Merge — dono se history alag dikhti hai
- Tags — releases ke liye versioning
- Stash — kaam beech mein rokh ke temporarily save karna

## 💻 Commands jo try kiye

### .gitignore
Repo mein `.gitignore` naam ki file banao, usme likho:
```
node_modules/
.env
*.log
dist/
.DS_Store
```
Ye files/folders Git track nahi karega, commit mein nahi aayenge.

### Commit message convention (Conventional Commits)
```
feat: add login functionality
fix: resolve navbar overlap issue
docs: update README with setup steps
chore: update dependencies
refactor: simplify auth logic
```
Format: `type: short description` — ye team projects mein history ko clean aur searchable banata hai.

### Rebase (advanced)
```bash
git rebase main              # apni branch ko main ke latest commits ke upar "replay" karta hai
git rebase -i HEAD~3            # interactive rebase — last 3 commits edit/squash/reorder kar sakte ho
```
**Merge vs Rebase:**
- `merge` → history mein branching dikhti hai (extra merge commit banta hai)
- `rebase` → history clean/linear dikhti hai (jaise sab ek hi line mein hua ho)

### Tags (versioning ke liye)
```bash
git tag v1.0.0                    # tag banata hai
git tag -a v1.0.0 -m "First release"  # annotated tag (message ke saath)
git push origin v1.0.0                # tag ko GitHub pe bhejta hai
git push origin --tags                  # saare tags push karta hai
```

### Stash (temporary save)
```bash
git stash                    # abhi ke changes temporarily save karta hai (working dir clean ho jaati hai)
git stash list                 # saare stashes dikhata hai
git stash pop                    # last stash wapas laata hai
git stash drop                     # stash delete karta hai
```

## 🎯 Challenge jo face kiya
- Rebase samajhna thoda tricky tha — practice se clear hua ki rebase history ko "rewrite" karta hai, isliye shared/public branches pe rebase avoid karna chahiye

## 📝 Key Takeaways
- `.gitignore` har project mein day-1 se hona chahiye (especially `.env` jaisi secret files ke liye)
- Clean commit messages future mein debugging aur code review dono ko aasan banate hain
- Rebase sirf apni local/feature branch pe use karo, kabhi shared main branch pe nahi
- Stash roz ke workflow mein bahut useful hai jab beech mein context switch karna pade

## 📌 Phase 1 (Git/GitHub/GitLab) Summary
Is 6-din mein maine seekha:
- Git ke core concepts (init, add, commit, branch, merge)
- GitHub pe collaboration (remote, push/pull, PRs, fork)
- GitLab overview aur CI/CD ka basic intro
- Real-world best practices (.gitignore, commit conventions, rebase, tags, stash)

## 🔜 Ab kya seekhunga
- Linux basics (Day 7 se shuru — already documented!)

---
*Day 6 of #100DaysOfDevOps*
