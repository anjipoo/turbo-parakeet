# mastering git

## commands so far 
1. `git init` 
- basic command to initialize git repo in the project folder
- creates .git dir that stores commit history, branches, config, tracking info

2. `git status`
- commmand to show current status of the git repo
- it tells which files changed, which are untracked, which branch you're on, pending commits

3. `git add <filename>`
- staged files for commit
- `git add .` for all files
eg. `git add README.md app.py requirements.txt`

4. `git commit -m "message"`
- all files in `git add` command are stored in your repo
- `-m` is for commit message: if using `git commit` only then git opens a text editor to put a commit message
- includes code snapshot, author info, timestamp, lines changed, unique hash id 