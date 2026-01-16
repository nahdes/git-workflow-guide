### Before you can commit, you need to stage your changes. Staging tells Git which changes you want to include in the next commit.

`git add filename.txt`

# Git: Staging and Committing Changes

Before you can commit, you need to **stage** your changes. Staging tells Git which changes you want to include in the next commit.

## Initialize a Git Repository

```bash
git init
```

This creates a hidden .git folder in your project directory. Run this only once per project.

## Stage Your Changes

### Stage a Single File

```bash
git add filename.txt
```

Use this to selectively add specific files to the staging area.

### Stage All Changes

```bash
git add .
```

This stages all new, modified, and deleted files in the current directory and subdirectories (except those ignored by .gitignore).

⚠️ Always review your changes before staging everything with `git add .`.

## Review Staged Changes

Check the status of your working directory:

```bash
git status
```

See exactly what will be committed:

```bash
git diff --staged
```

To view unstaged changes:

```bash
git diff
```

## Commit the Staged Changes

```bash
git commit -m "Your descriptive commit message"
```

## Good Examples

```bash
git commit -m "Add user login validation"
git commit -m "Fix crash when submitting empty form"
```

## Avoid Vague Messages

```bash
git commit -m "update" # ❌ Too vague
git commit -m "fixed stuff" # ❌ Unhelpful
```

## Best Practices for Commit Messages

- Use the imperative mood: “Add”, “Fix”, “Update”
- Keep the first line under 72 characters
- For complex changes, add a body after a blank line (use `git commit` without `-m`)

## Full Workflow Example

```bash
# 1. Initialize (once)
git init

# 2. Make changes to your files...

# 3. Stage changes
git add .

# OR stage specific files
# git add src/app.js

# 4. Review
git status
git diff --staged

# 5. Commit
git commit -m "Initial commit with project setup"

# 6. Add remote and push (after first commit)
git remote add origin https://github.com/username/repo.git
git push -u origin main
```

## Pro Tips

- Use `git add -p` to stage changes hunk by hunk.
- Never run `git add .` without checking `git status` first.
- Set your identity globally (do once):

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

- After your first commit, connect to a remote repo:

```bash
git remote add origin https://github.com/username/repo.git
git push -u origin main
```

💡 A great commit is atomic, clear, and reversible — treat it like a small, meaningful story.

# Comment Amending

```bash
 git commit --amend
```
