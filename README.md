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
- eg. `git add README.md app.py requirements.txt`

4. `git commit -m "message"`
- all files in `git add` command are stored in your repo
- `-m` is for commit message: if using `git commit` only then git opens a text editor to put a commit message
- includes code snapshot, author info, timestamp, lines changed, unique hash id 

5. `git log`
- shows commit history of repo
- eg. output
    ```bash
    commit 76ba1bb3a14a773412adda1654bff8e24dfe7dd4 (HEAD -> main, origin/main)
    Author: anjipoo <anjanarajagopal2004@gmail.com>
    Date:   Wed May 27 15:25:20 2026 +0530

        first commit
    ```
- to get log in 1 line: `git log --oneline`
- eg. output
    ```bash
    76ba1bb (HEAD -> main, origin/main) first commit
    ```
- best view to see as a tree: `git log --graph --oneline --all`

6. `git branch`
- see all branches 
- output shows all branches 
- * mark against the current branch

7. `git branch <branchname>`
- creates a new branch
- DOES NOT switch to that branch
- switching using `git checkout <branchname>`
- create + switch in 1 step: `git checkout -b feature-login`

8. `git remote add origin <url>`
- connects repo to github/gitlab/bitbucket
- eg. `git remote add origin https://github.com/anjipoo/turbo-parakeet.git`
- parts:
    a. `git remote` - manages remote repo
    b. `add` - adds new connection
    c. `origin` - name of remote 
    d. `<url>` - link of your repo

9. `git remote -v`
- shows the remote repos connected to your local git proj
- eg. output
    ```bash
    origin  https://github.com/anjipoo/turbo-parakeet.git (fetch)
    origin  https://github.com/anjipoo/turbo-parakeet.git (push)
    ```
- `-v` stands for verbose, without it the command will only return name. 

10. `git push -u origin main`
- uploads to the remote repo
- parts:
    a. `git push` - sends commit to remote
    b. `origin` - name of remote
    c. `main` - branch you're pushing (if pushing a new branch then `git push -u origin <branchname>`)
    d. `-u` - upstream--links local main to origin/main

11. `git switch <branchname>`
- used to switch between branches 

12. `git checkout -b <branchname>`
- creates a new branch AND switches to it
- equivalent to 
    ```bash
    git branch <branchname>
    git switch <branchname>
    ```

13. `git diff`
- shows exact changes line by line
- red shows removed lines, green shows added lines

14. `git merge <branchname> -m "message"`
- after making changes to other branch, switch to main branch and run this command
- merges and combines branch history
- to check if branch merged or not, run `git log --oneline --graph --all` and see the merge commit 

^nice^ why am i even doing this man ugh