# ultimate-git-github-guide-smit

# 🚀 Ultimate Git & GitHub Guide

> Beginner Friendly Git & GitHub Guide for SMIT Students & Developers 🚀

---

# 🌐 Language

- [🇵🇰 Roman Urdu Guide](#-roman-urdu-guide)
- [🇺🇸 English Guide](#-english-guide)

---

# 🇵🇰 Roman Urdu Guide

# 🧐 1. Git vs GitHub — Asaan Alfaaz Mein

| Git | GitHub |
|------|--------|
| Aapke computer ka Version Control System | Online Cloud Platform |
| Code ki history save karta hai | Code ko internet par store karta hai |
| Offline bhi kaam karta hai | Internet required hota hai |
| Local machine par kaam karta hai | Online repositories manage karta hai |

---

# 🛠️ 2. First-Time Setup (New PC ya New Project)

Agar aap:

- Naye PC par hain
- Ya pehli baar Git use kar rahe hain

toh ye setup karein.

---

## ✅ Step 1 — Apni Identity Set Karein

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

### Example

```bash
git config --global user.name "Fahad Bin Junaid"
git config --global user.email "example@gmail.com"
```

---

## ✅ Step 2 — Login Helper Enable Karein

Agar GitHub login popup na aaye ya authentication issue ho:

### Recommended Command

```bash
git config --global credential.helper manager
```

### Agar upar wali kaam na kare toh:

```bash
git config --global credential.helper wincred
```

---

# 🔄 3. Simple Git Workflow

```text
Code Write
   ↓
git status
   ↓
git add .
   ↓
git commit -m "message"
   ↓
git push
   ↓
GitHub Updated ✅
```

---

# 📝 4. Daily Git Workflow (Correct Sequence)

---

## ✅ Step 1 — Git Initialize Karein

⚠️ Sirf ek baar new project mein use hota hai.

```bash
git init
```

---

## ✅ Step 2 — Files Status Check Karein

```bash
git status
```

Ye batata hai:

- Kaunsi files change hui hain
- Kaunsi files staged hain

---

## ✅ Step 3 — Files Staging Area Mein Add Karein

```bash
git add .
```

Ye saari files staging area mein bhejta hai.

---

## ✅ Step 4 — Snapshot Save Karein (Commit)

```bash
git commit -m "Assignment Completed"
```

Example:

```bash
git commit -m "Added README guide"
```

---

## ✅ Step 5 — Branch Name Main Rakhein

⚠️ Usually sirf pehli baar zaroori hota hai.

```bash
git branch -M main
```

---

## ✅ Step 6 — GitHub Repository Connect Karein

```bash
git remote add origin YOUR_REPOSITORY_URL
```

### Example

```bash
git remote add origin https://github.com/username/repository-name.git
```

---

## ✅ Step 7 — GitHub Par Upload Karein

```bash
git push -u origin main
```

⚠️ First push par login popup aa sakta hai.

Successfully login karne ke baad code GitHub par upload ho jayega.

---

# 🔄 5. Future Updates Kaise Karein

Agar project already connected hai toh future mein sirf ye commands chalani hoti hain:

```bash
git status
git add .
git commit -m "Updated project"
git push
```

---

# 📥 6. Existing Repository Par Kaam Kaise Karein

Agar repository pehle se GitHub par hai toh:

---

## ✅ Step 1 — Repository Download Karein

```bash
git clone REPOSITORY_URL
```

### Example

```bash
git clone https://github.com/username/project.git
```

---

## ✅ Step 2 — Folder Open Karein

```bash
cd project-name
```

---

## ✅ Step 3 — Kaam Karein Aur Upload Karein

```bash
git status
git add .
git commit -m "Updated project"
git push
```

---

# 🔄 7. Important Git Commands Difference

---

## ✅ git clone

GitHub repository ko computer par download karta hai.

```bash
git clone REPOSITORY_URL
```

---

## ✅ git pull

GitHub se latest updates download karta hai.

```bash
git pull
```

⚠️ Team projects mein kaam start karne se pehle use karein.

---

## ✅ git push

Apna local code GitHub par upload karta hai.

```bash
git push
```

---

## ✅ git status

Files ka current status check karta hai.

```bash
git status
```

---

## ✅ git log

Commit history show karta hai.

```bash
git log
```

---

## ✅ git restore

File changes discard karta hai.

```bash
git restore filename
```

---

# 🖥️ 8. GitHub Desktop (Optional)

GitHub Desktop ek graphical application hai jo Git commands ko buttons ke through use karne deta hai.

Useful for beginners who terminal pasand nahi karte.

## Official Website

https://desktop.github.com/

## Features

- Clone repositories
- Push code
- Pull updates
- Easy login
- Commit changes
- Beginner friendly interface

---

# 🔐 9. Work End — Logout & Security Guide

---

# 💻 Personal PC vs Shared PC

## ✅ Personal PC (Apna Laptop / Computer)

Agar aap apne personal laptop ya computer par kaam kar rahe hain:

✅ Logout karna zaroori nahi hota.

Aap simply window close kar sakte hain.

---

## 🏫 Shared PC (SMIT Lab / Friend PC / Public Computer)

⚠️ Agar aap:

- SMIT Lab
- Friend ka PC
- Public Computer

use kar rahe hain toh logout karna bohat zaroori hai.

Warna doosra banda aapke GitHub account ka access use kar sakta hai.

---

# 🚪 10. Shared PC Logout Process

---

## ✅ Step 1 — Git Identity Remove Karein

```bash
git config --global --unset user.name
git config --global --unset user.email
git config --global --unset credential.helper
```

---

## ✅ Step 2 — Windows Credential Manager Se Login Remove Karein

### Follow These Steps

1. Windows Search open karein
2. Search karein:

```text
Credential Manager
```

3. Open karein:

```text
Windows Credentials
```

4. Niche list mein ye dhoondein:

```text
git:https://github.com
```

5. Usko select karke:

```text
Remove
```

par click karein.

---

# ✅ Step 3 — Verification

Terminal mein ye command chalayein:

```bash
git fetch
```

YA

```bash
git ls-remote
```

Agar login popup dobara khul jaye:

✅ Matlab account successfully logout ho gaya hai.

---

# ⚠️ 11. Important Security Tips

⚠️ Never share:

- GitHub Password
- Personal Access Token (PAT)

with anyone.

---

# ❌ 12. Common Errors & Solutions

---

## ❌ Error

```text
src refspec main does not match any
```

## ✅ Fix

```bash
git add .
git commit -m "First Commit"
```

Phir dobara push karein.

---

## ❌ Error

```text
Authentication failed
```

## ✅ Fix

```bash
git config --global credential.helper manager
```

Phir dobara login karein.

---

## ❌ Error

```text
remote origin already exists
```

## ✅ Fix

```bash
git remote remove origin
```

Phir naya repository URL add karein.

---

# 🎯 Recommended Repository Names

- ultimate-git-github-guide
- git-github-for-beginners
- git-workflow-guide
- git-security-guide
- smit-git-guide
- ultimate-git-github-guide-smit

---

# 🇺🇸 English Guide

# 🧐 Git vs GitHub

| Git | GitHub |
|------|--------|
| Local Version Control System | Cloud Platform |
| Tracks code history | Stores repositories online |
| Works offline | Requires internet |
| Runs on your computer | Runs on the web |

---

# 🛠️ First-Time Setup

## Set Your Identity

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

---

## Enable Credential Helper

```bash
git config --global credential.helper manager
```

---

# 🔄 Basic Workflow

```text
Write Code
   ↓
git status
   ↓
git add .
   ↓
git commit -m "message"
   ↓
git push
   ↓
GitHub Updated ✅
```

---

# 📥 Clone Existing Repository

```bash
git clone REPOSITORY_URL
```

---

# 🔄 Important Commands

| Command | Purpose |
|----------|----------|
| git clone | Download repository |
| git pull | Get latest updates |
| git push | Upload code |
| git status | Check file status |
| git log | View commit history |

---

# 🔐 Shared PC Security

If you are using:

- Lab Computer
- Friend PC
- Public Computer

Always logout after work.

---

## Remove Git Identity

```bash
git config --global --unset user.name
git config --global --unset user.email
git config --global --unset credential.helper
```

---

## Remove GitHub Credentials

Open:

```text
Credential Manager → Windows Credentials
```

Remove:

```text
git:https://github.com
```

---

# ⚠️ Security Tip

Never share your:

- GitHub Password
- Personal Access Token (PAT)

---

# 👨‍💻 Guide Created By

**Fahad Bin Junaid** 🚀
