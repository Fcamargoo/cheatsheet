
# Git Cheat Sheet
<p>Git is the free and open source distributed version control system that's responsible for everything GitHub
related that happens locally on your computer. This cheat sheet features the most important and commonly
used Git commands for easy reference.</p>

_____

**INSTALLATION & GUIS**
With platform specific installers for Git, GitHub also provides the
ease of staying up-to-date with the latest releases of the command
line tool while providing a graphical user interface for day-to-day
interaction, review, and repository synchronization.

____

**GitHub for Windows**<br>
htps://windows.github.com<br>
**GitHub for Mac**<br>
htps://mac.github.com<br>
**For Linux and Solaris platforms, the latest release is available on
the official Git web site.**<br>
**Git for All Platforms**<br>
htp://git-scm.com
____
<div>
<details>
<summary><strong>STAGE & SNAPSHOT</strong></br>
Working with snapshots and the Git staging area</summary>
</br>
<strong>git status</strong></br>
show modified files in working directory, staged for your next commit
</br>
</br>
<strong>git add [file]</strong></br>
add a file as it looks now to your next commit (stage)
</br>
</br>
<strong>git reset [file]</strong></br>
unstage a file while retaining the changes in working directory
</br>
</br>
<strong>git diff</strong><br>
diff of what is changed but not staged
<br>
</br>
<strong>git diff --staged</strong><br>
diff of what is staged but not yet commited
<br>
</br>
<strong>git commit -m “[descriptive message]”</strong><br>
commit your staged content as a new commit snapshot<br>
</details>
<div>

____

<div>
<details>
<summary><strong>SETUP</strong><br>
Configuring user information used across all local repositories</summary>
<br>
<strong>git config --global user.name “[firstname lastname]”</strong>
set a name that is identifiable for credit when review version history
<br>
</br>
<strong>git config --global user.email “[valid-email]”</strong><br>
set an email address that will be associated with each history marker
<br>
</br>
<strong>git config --global color.ui auto</strong><br>
set automatic command line coloring for Git for easy reviewing
<br>
</details>
</div>

____

<div>
<details>
<summary><strong>BRANCH & MERGE</strong><br>
Isolating work in branches, changing context, and integrating changes</summary>
<br>
<strong>git branch</strong><br>
list your branches. a * will appear next to the currently active branch
<br>
<br>
<strong>git branch [branch-name]</strong><br>
create a new branch at the current commit
<br>
<br>
<strong>git checkout</strong><br>
switch to another branch and check it out into your working directory
<br>
<br>
<strong>git merge [branch]</strong><br>
merge the specified branch’s history into the current one
<br>
<br>
<strong>git log</strong><br>
show all commits in the current branch’s history
<br>
</details>
</div>

____

<div>
<details>
<summary><strong>SETUP & INIT</strong><br>Configuring user information, initializing and cloning repositories</summary><br>
<strong>git init</strong><br>
initialize an existing directory as a Git repository
<br>
<br>
<strong>git clone [url]</strong><br>
retrieve an entire repository from a hosted location via URL
<br>
</details>
</div>

____

<div>
<details>
<summary><strong>INSPECT & COMPARE</strong><br>Examining logs, diffs and object information</summary><br>
<strong>git log</strong><br>
show the commit history for the currently active branch
<br>
<br>
<strong>git log branchB..branchA</strong><br>
show the commits on branchA that are not on branchB
<br>
<br>
<strong>git log --follow [file]</strong><br>
show the commits that changed file, even across renames
<br>
<br>
<strong>git diff branchB...branchA</strong><br>
show the diff of what is in branchA that is not in branchB
<br>
<br>
<strong>git show [SHA]</strong><br>
show any object in Git in human-readable format
<br>
</details>
</div>

____

<div>
<details>
<summary><strong>TRACKING PATH CHANGES</strong><br>Versioning file removes and path changes</summary><br>
<strong>git rm [file]</strong><br>
delete the file from project and stage the removal for commit
<br>
<br>
<strong>git mv [existing-path] [new-path]</strong><br>
change an existing file path and stage the move
<br>
<br>
<strong>git log --stat -M</strong><br>
show all commit logs with indication of any paths that moved
<br>
</details>
</div>

____

<div>
<details>
<summary><strong>SHARE & UPDATE</strong><br>Retrieving updates from another repository and updating local repos</summary><br>
<strong>git remote add [alias] [url]</strong><br>
add a git URL as an alias
<br>
<br>
<strong>git fetch [alias]</strong><br>
fetch down all the branches from that Git remote
<br>
<br>
<strong>git merge [alias]/[branch]</strong><br>
merge a remote branch into your current branch to bring it up to date
<br>
<br>
<strong>git push [alias] [branch]</strong><br>
Transmit local branch commits to the remote repository branch
<br>
<br>
<strong>git pull</strong><br>
fetch and merge any commits from the tracking remote branch
<br>
</details>
</div>

____

<div>
<details>
<summary><strong>REWRITE HISTORY</strong><br>Rewriting branches, updating commits and clearing history</summary><br>
<strong>git rebase [branch]</strong><br>
apply any commits of current branch ahead of specified one
<br>
<br>
<strong>git reset --hard [commit]</strong><br>
clear staging area, rewrite working tree from specified commit
<br>
</details>
</div>

____

<div>
<details>
<summary><strong>TEMPORARY COMMITS</strong><br>Temporarily store modified, tracked files in order to change branches</summary><br>
<strong>git stash</strong><br>
Save modified and staged changes
<br>
<br>
<strong>git stash list</strong><br>
list stack-order of stashed file changes
<br>
<br>
<strong>git stash pop</strong><br>
write working from top of stash stack
<br>
<br>
<strong>git stash drop</strong><br>
discard the changes from top of stash stack<br>
</details>
</div>

____

<div>
<details>
<summary><strong>IGNORING PATTERNS</strong><br>Preventing unintentional staging or commiting of files</summary><br>
<strong>logs/
*.notes
pattern*/</strong><br>
Save a file with desired paterns as .gitignore with either direct string
matches or wildcard globs.
<br>
<br>
<strong>git config --global core.excludesfile [file]</strong><br>
system wide ignore patern for all local repositories
<br>

____

