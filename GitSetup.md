
---

#  **Complete Git Setup Guide for Windows CMD**

---

##  1. What is Git?

**Git** is a distributed version control system that tracks changes in your files (usually code).
It allows multiple people to collaborate efficiently on the same project.

---

##  2. Installing Git

1. Visit [https://git-scm.com/](https://git-scm.com/)
2. Download the latest version for Windows
3. Run the installer
4. During setup, **check the box** to “Add Git Bash to PATH”
5. Finish installation

---

##  3. Check Git Installation

Open **Command Prompt (CMD)** or **PowerShell** and type:

```bash
git --version
```

 Output example:

```
git version 2.45.0.windows.1
```

If you see this, Git is correctly installed.

---

##  4. Setting Up Git for the First Time

Git needs your identity (name and email) for commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

* `--global` means this applies to all repositories on your computer.
* Omit `--global` if you want to set it only for a specific repository.

 **Example**

```bash
git config --global user.name "Jane Doe"
git config --global user.email "jane@example.com"
```

---

##  5. Verify Your Git Configuration

To see all settings:

```bash
git config --list
```

To check specific values:

```bash
git config user.name
git config user.email
```

---

##  6. Set Default Branch Name

Modern Git prefers **main** instead of **master**.
Set it once globally:

```bash
git config --global init.defaultBranch main
```

---

##  7. Manage Git Credentials

If you use HTTPS for GitHub, GitLab, etc., you can store login info.

**Option 1: Store credentials in plain text**

```bash
git config --global credential.helper store
```

**Option 2: Use Windows Credential Manager (recommended)**

```bash
git config --global credential.helper manager
```

---

##  8. Configure Proxy (if needed)

If you are behind a corporate proxy, use:

```bash
git config --global http.proxy http://proxyuser:proxypassword@proxy.server.com:port
```

Unset proxy:

```bash
git config --global --unset http.proxy
```

---

##  9. Set Git Path in Environment Variables (if Git not recognized)

If `git` command doesn’t work in CMD:

1. Press **Win + S** → type **Environment Variables**
2. Open **Edit the system environment variables**
3. Click **Environment Variables**
4. Under **System Variables**, find `Path` → click **Edit**
5. Add this path (default Git install path):

   ```
   C:\Program Files\Git\bin
   C:\Program Files\Git\cmd
   ```
6. Click **OK** → Restart CMD

Now try:

```bash
git --version
```

---

##  10. Initialize a New Git Repository

Create a new project:

```bash
mkdir myproject
cd myproject
git init
```

 Creates a hidden `.git` folder — your repository.

---

##  11. Basic Git Commands

| Command                   | Description              |
| ------------------------- | ------------------------ |
| `git init`                | Initialize a repository  |
| `git clone <url>`         | Clone a remote repo      |
| `git status`              | Check file changes       |
| `git add <file>`          | Stage a file for commit  |
| `git add .`               | Stage all changes        |
| `git commit -m "message"` | Commit with a message    |
| `git log`                 | View commit history      |
| `git push origin main`    | Upload commits to remote |
| `git pull origin main`    | Download latest changes  |

---

## 12. View, Edit, or Remove Configuration

### View all configs:

```bash
git config --list
```

### Edit config manually:

```bash
git config --global --edit
```

### Unset a config:

```bash
git config --global --unset user.name
```

---

## 13. Useful Global Aliases (optional)

Make Git commands shorter:

```bash
git config --global alias.st status
git config --global alias.cm "commit -m"
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.lg "log --oneline --graph --all"
```

Now you can type:

```bash
git st
git cm "message"
git lg
```

---

## 14. Backup and Export Git Config

To export your global config file:

```bash
notepad "%USERPROFILE%\.gitconfig"
```

You can copy this file to another system to keep your Git setup consistent.

---

## 15. Notes

| Purpose                | Command                                                  |
| ---------------------- | -------------------------------------------------------- |
| Check Git version      | `git --version`                                          |
| Set user name          | `git config --global user.name "Your Name"`              |
| Set email              | `git config --global user.email "youremail@example.com"` |
| Default branch         | `git config --global init.defaultBranch main`            |
| Check configuration    | `git config --list`                                      |
| Set credential manager | `git config --global credential.helper manager`          |
| Set PATH (if needed)   | Add `C:\Program Files\Git\cmd` to environment variables  |

---

