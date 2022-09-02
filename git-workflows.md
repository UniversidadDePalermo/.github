# Git Workflow

## Downloading a Repository

Whenever you want to download a repository for the first time, you must `clone`
it using the `git clone` command.

```bash
git clone <url>
```

E.g.

```bash
git clone https://github.com/up-prog/python.git
```

This will create a directory with the repository name, in this case it is
`python` (the text before `.git`) in the URL above.

## Creating a Branch

Usually you create a branch whenever you want to perform changes in the source
code, this way you keep your own version of the repository. To create a new
branch you use `git checkout` command along with the `-b` option.

```bash
git checkout -b
```

Then you provide the name of your branch, branches should be lowercase,
can't include any spaces and its recommended to keep them short.

E.g.

```bash
git checkout -b feat/support-for-mobile-phone
```

```bash
git checkout -b fix/invalid-request-sent-to-server
```

> Similar to commit messages, we use `fix` and `feat` for our branch names followed by a slash.

## Pushing Changes to GitHub

1. Add files to the stash

```bash
git add .
```

2. Commit files providing a message. The message must describe the changes
introduced in the commit.

E.g.

When a new feature is introduced, the commit message must start with
`feat` (from feature).

```
feat: support to update username
```

When a bug fix is introduced, the commit message must start with `fix`
(from fix).

```
fix: invalid date parsing
```

3. Finally you must push the commit to GitHub

```bash
git push origin <branch>
```

E.g.

```bash
git push origin feat/profile-settings
```
