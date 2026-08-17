# Day 04 - GitHub Deep Dive

## 📖 Kya seekha
- GitHub Git repos ko cloud pe host karta hai — team collaboration ke liye
- **Remote repository** kya hoti hai aur local repo se kaise connect hoti hai
- Pull Requests (PRs) collaboration ka core workflow hain
- Fork vs Clone ka difference

## 💻 Commands jo try kiye

### Remote connect karna
```bash
git remote add origin <repo-url>     # remote add karta hai (naam "origin")
git remote -v                          # saare remotes list karta hai (fetch/push URLs)
git remote remove origin                 # remote hata deta hai
```

### Push & Pull
```bash
git push origin main              # local commits ko GitHub pe bhejta hai
git push -u origin main             # upstream set karta hai (aage sirf "git push" kaafi hoga)
git pull origin main                  # GitHub se latest changes local mein laata hai
git fetch origin                        # changes download karta hai bina merge kiye
```

### Cloning
```bash
git clone <repo-url>              # GitHub repo ko local mein copy karta hai (poori history ke saath)
```

## 🌟 GitHub Workflow (Team collaboration)

1. **Fork** — kisi doosre ke repo ki apni copy banao (apne account mein)
2. **Clone** — apna fork local machine pe laao
3. **Branch** banao naya feature ke liye
4. Changes karo, commit karo, **push** karo apne fork mein
5. GitHub pe **Pull Request (PR)** kholo — original repo ke owner ko batata hai "mera code merge karo"
6. Owner review karta hai, comments deta hai, phir **merge** karta hai

## 🎯 Challenge jo face kiya
- Fork vs Clone samajhne mein confusion hua — Fork ek naya copy hai GitHub pe (apne account mein), Clone us repo (fork ya original) ko local machine pe laata hai

## 📝 Key Takeaways
- `origin` bas ek naam hai remote URL ke liye — koi bhi naam use kar sakte hain
- PRs sirf code merge karne ka tarika nahi, balki **code review** ka bhi tool hain
- Open source contribution ka standard flow: Fork → Clone → Branch → PR

## 🔜 Kal kya seekhunga
- GitLab — overview aur GitHub se comparison

---
*Day 4 of #100DaysOfDevOps*
