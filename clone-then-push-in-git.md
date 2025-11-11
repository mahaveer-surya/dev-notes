
---

# **Clone Repository, Make Changes, and Push to Remote**

---

## 1. What This Does

This process is used when you already have a **remote repository** (e.g., on GitHub)
and you want to **clone it to your local machine**, make edits, and then **push updates back** to the remote.

---

## 2. Clone the Remote Repository

Navigate to the folder where you want to copy the project:

```bash
cd path\to\your\workspace
```

Clone the repository:

```bash
git clone https://github.com/username/repo-name.git
```

Example output:

```
Cloning into 'repo-name'...
remote: Enumerating objects...
Receiving objects: 100% (20/20), done.
```

Move into the cloned project folder:

```bash
cd repo-name
```

---

## 3. Check the Remote Connection

Verify that your local copy is linked to the correct remote repository:

```bash
git remote -v
```

Example:

```
origin  https://github.com/username/repo-name.git (fetch)
origin  https://github.com/username/repo-name.git (push)
```

If not linked, you can manually set it:

```bash
git remote add origin https://github.com/username/repo-name.git
```

---

## 4. Make Changes to the Project

Edit or add files in your cloned project.

Then check which files have changed:

```bash
git status
```

---

## 5. Stage and Commit Changes

Stage all modified files:

```bash
git add .
```

Commit your changes with a message:

```bash
git commit -m "Updated files and fixed issues"
```

---

## 6. Pull Latest Changes (Before Pushing)

Always pull the latest version from the remote first
(to avoid conflicts if someone else has pushed changes):

```bash
git pull origin main
```

---

## 7. Push Your Changes to Remote Repository

Now push your updates:

```bash
git push origin main
```

If this is the first time pushing from this branch, use:

```bash
git push -u origin main
```

---

## 8. Verify Your Push

Check on your GitHub / GitLab repository —
you should now see your updated files and commits

---

## 9. Common Commands

| Purpose                 | Command                            |
| ----------------------- | ---------------------------------- |
| Clone remote repo       | `git clone <repo-url>`             |
| Enter project directory | `cd repo-name`                     |
| Check remote URL        | `git remote -v`                    |
| Add remote (if missing) | `git remote add origin <repo-url>` |
| Check file changes      | `git status`                       |
| Stage files             | `git add .`                        |
| Commit changes          | `git commit -m "message"`          |
| Pull latest version     | `git pull origin main`             |
| Push changes to remote  | `git push origin main`             |

---
