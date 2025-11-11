
---

# **Send Local Project to Remote Repository**

---

## 1. Prerequisites

Make sure you have:

* Git installed and configured (`git --version`)
* A GitHub / GitLab / Bitbucket account
* A **remote repository** already created on that platform (empty)

Example remote URL formats:

* **HTTPS:** `https://github.com/username/repo-name.git`
* **SSH:** `git@github.com:username/repo-name.git`

---

## 2. Initialize Git in Your Local Project

If your project folder isn’t yet a Git repository:

```bash
cd path\to\your\project
git init
```

This creates a hidden `.git` folder — it tells Git to start tracking the project.

---

## 3. Add and Commit Files

Stage all files for tracking:

```bash
git add .
```

Commit with a message:

```bash
git commit -m "Initial commit"
```

---

## 4. Add the Remote Repository

Link your local project to the remote repo:

```bash
git remote add origin https://github.com/username/repo-name.git
```

Verify connection:

```bash
git remote -v
```

You should see something like:

```
origin  https://github.com/username/repo-name.git (fetch)
origin  https://github.com/username/repo-name.git (push)
```

---

## 5. Set the Default Branch Name (if needed)

If your repo uses **main** (recommended):

```bash
git branch -M main
```

---

## 6. Push Local Project to Remote Repository

Upload your local commits to the remote:

```bash
git push -u origin main
```

Explanation:

* `origin` = name of the remote repo
* `main` = branch name
* `-u` sets tracking so you can later just use `git push` and `git pull`

---

## 7. Verify on Remote

Go to your GitHub (or GitLab) repository page —
you should now see all your project files there 

---

## 8. Common Commands 

| Purpose                  | Command                            |
| ------------------------ | ---------------------------------- |
| Initialize Git repo      | `git init`                         |
| Stage all files          | `git add .`                        |
| Commit files             | `git commit -m "message"`          |
| Add remote               | `git remote add origin <repo-url>` |
| Rename branch to main    | `git branch -M main`               |
| Push project to remote   | `git push -u origin main`          |
| Verify remote connection | `git remote -v`                    |

---

