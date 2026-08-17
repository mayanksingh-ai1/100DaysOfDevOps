# Day 05 - GitLab Overview

## 📖 Kya seekha
- GitLab bhi GitHub jaisa hi ek **Git hosting platform** hai
- GitLab ka bada focus **built-in CI/CD** pe hai (DevOps ke liye important)
- Companies mein dono use hote hain — GitHub zyada open-source/community ke liye popular, GitLab enterprise/self-hosted DevOps pipelines ke liye zyada use hota hai

## 🔍 GitHub vs GitLab

| Feature | GitHub | GitLab |
|---------|--------|--------|
| Owner | Microsoft | GitLab Inc. |
| CI/CD | GitHub Actions (add-on) | Built-in CI/CD (core feature) |
| Self-hosting | GitHub Enterprise (paid) | GitLab CE free & easy self-host |
| Community/Open Source | Bahut bada, most popular | Chota but growing |
| Issue tracking | Yes | Yes (thoda zyada powerful/built-in) |
| Free private repos | Yes | Yes |

## 💻 GitLab basics (commands same hain, kyunki dono Git use karte hain)
```bash
git remote add origin https://gitlab.com/username/repo.git
git push -u origin main
```
Git commands GitHub aur GitLab dono ke liye **same** hote hain — sirf remote URL alag hoti hai, kyunki underlying tool "Git" hi hai.

## 🚀 GitLab CI/CD Intro (basic concept)
GitLab mein repo ke root mein `.gitlab-ci.yml` file daal ke pipeline define kar sakte hain:
```yaml
stages:
  - build
  - test

build-job:
  stage: build
  script:
    - echo "Building the app..."

test-job:
  stage: test
  script:
    - echo "Running tests..."
```
Ye file jaise hi push hoti hai, GitLab automatically **pipeline run** kar deta hai — isko hum Phase 2 mein CI/CD topic mein detail se seekhenge.

## 🎯 Challenge jo face kiya
- Samajhna tha ki GitLab aur GitHub "competitors" nahi, balki dono **Git hosting services** hain jo same underlying tool (Git) use karte hain — bas platform-specific features alag hain

## 📝 Key Takeaways
- Git = tool, GitHub/GitLab = hosting platforms (jaise Gmail aur Outlook dono email use karte hain but companies alag hain)
- DevOps roles mein dono ka use dekhne ko milta hai — company pe depend karta hai
- GitLab ka CI/CD built-in hona isse DevOps pipelines ke liye ek natural choice banata hai

## 🔜 Kal kya seekhunga
- Git best practices — .gitignore, commit conventions, workflows

---
*Day 5 of #100DaysOfDevOps*
