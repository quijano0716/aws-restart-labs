# AWS re/Start — Lab Reports

Technical documentation of hands-on labs completed during the **AWS re/Start** program.

## 🔗 View Online

👉 **[Open Lab Reports](https://<your-username>.github.io/aws-restart-labs/)**

> Replace `<your-username>` with your GitHub username once Pages is configured.

## 📋 Labs

| #  | Lab                           | Status       |
|----|-------------------------------|--------------|
| 01 | Introduction to Amazon EC2    | ✅ Completed  |
| 02 | —                             | ⏳ Pending    |
| 03 | —                             | ⏳ Pending    |

## 📂 Project Structure

```
aws-restart-labs/
├── docs/                    ← GitHub Pages serves from here
│   ├── index.html           ← Main landing page
│   ├── lab-01-ec2/
│   │   ├── index.html
│   │   └── assets/screenshots/
│   ├── lab-02-.../
│   └── lab-03-.../
└── README.md
```

## ⚙️ Setting Up GitHub Pages

1. Push this repository to GitHub
2. Go to **Settings → Pages**
3. Under "Source", select **Deploy from a branch**
4. Under "Branch", select `main` and the `/docs` folder
5. Save and wait ~1 minute

## ➕ Adding a New Lab

1. Create a folder inside `docs/`, e.g.: `docs/lab-04-s3/`
2. Add your `index.html` and `assets/` folder inside
3. Edit `docs/index.html` to add the new lab card
4. Run `git add .`, `git commit`, and `git push`
5. GitHub Pages updates automatically

---

**Student:** Julian David Quijano  
**Program:** AWS re/Start
