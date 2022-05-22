# Git-Cheat-Sheet






# A) Definitions:

1. **Working Tree**: Current files
2. **Staged**: Files related to be comitted




# B) Creating Projects:


### B-1) `clone`:
To clone a create a local copy from a remote repo.

<b>

```
git clone <remote_location>
```
</b>


### B-2) `init`:
To create a new Repo.


<b>


```
git init
```
</b>







# C) Basic Snapshotting:


### C-1) `add`:

prepare the content staged for the next commit.


<table>
<tr>
<th>

`git add .`

</th>
<td>make all files staged</td>
</tr>
<tr>
<th>

`git add <file_location>`

</th>
<td>make file staged</td>
</tr>
</table>







### C-2) `status`:

Display the differnce between working tree and the current HEAD commit, files that are not tracked.


<b>

```
git status
```
</b>





### C-3) `diff`:



Show changes.




<table>
<tr>
<th>

`git diff`

</th>
<td>
Getting differnence between working and current HEAD
</td>
</tr>
<tr>
<th>

`git diff <commit_SHA>`

</th>
<td>
Getting differnence between working and the commit
</td>
</tr>
<tr>
<th>

`git diff <commit_SHA> -- <file_path>`

</th>
<td>
Getting differnence between working and the commit for a specific file
</td>
</tr>
<tr>
<th>

`git diff topic master`

`git diff topic..master`

`git diff topic...master`


</th>
<td>
Comparing Branches
</td>
</tr>
</table>







### C-4) `commit`:




Commit changes to git.




<table>
<tr>
<th>

`git commit`

</th>
<td>
Commit all staged files
</td>
</tr>
<tr>
<th>

`git commit -m "message"`

</th>
<td>
Commit all staged files with a message
</td>
</tr>
<tr>
<th>

`git commit -a (--all) -m "message"`

</th>
<td>
Stage all files and commit them with a message
</td>
</tr>
<tr>
<th>

`git commit --file <file_path>`



</th>
<td>
Commit all staged files with a message from a file
</td>
</tr>
</table>










### C-5) `restore`:

Restores specified files of the working tree from the last commit.






<table>
<tr>
<th>

`git restore <file_path>`

</th>
<td>
Restore file from last commit
</td>
</tr>
<tr>
<th>

`git restore --staged <file_path>`

</th>
<td>
Remove file from staging area
</td>
</tr>
<tr>
<th>

`git restore --source <source SHA> <file_path>`

</th>
<td>
Restores file from a specific commit
</td>
</tr>
</table>












### C-6) `reset`:

Resets the working tree to the specified commit, and removes the following commits.  

It has modes:





<table>


<tr>
<th>Mode</th>
<th>Working Tree</th>
</tr>

<tr>
<th>--soft</th>
<td>Staged</td>
</tr>

<tr>
<th>--hard</th>
<td>restored</td>
</tr>


<tr>
<th>--mixed (default)</th>
<td>Intact</td>
</tr>

</table>










<table>

<tr>
<th>

`git reset <commit_SHA>`
</th>
</tr>



<tr>
<th>

`git reset <commit_SHA> [--mode]`
</th>
</tr>
</table>













### C-6) `rm`:

Remove files from the working tree, and stage changes.


**`git rm <file_path>`**


















# D) Branching and Merging:


### D-1) `branch`:
List, create or delete branches.




<table>
<tr>
<th>

`git branch`
</th>
<td>
List all branches
</td>
</tr>
<tr>
<th>

`git branch <branch_name>`

</th>
<td>
Create a new branch
</td>
</tr>
<tr>
<th>

`git branch -d (--delete) <branch_name>`

</th>
<td>
Delete a branch
</td>
</tr>
<tr>
<th>

`git branch <branch_name> <commit_SHA>`
</th>
<td>
Create a branch from a commit
</td>
</tr>


<tr>
<th>

`git branch -m (--move) <old_branch_name> <new_branch_name>`
</th>
<td>
Rename a branch
</td>
</tr>

<tr>
<th>

`git branch --copy <old_branch_name> <new_branch_name>`
</th>
<td>
Copy a branch
</td>


</table>






### D-2) `checkout`:

Change the current branch.




<table>
<tr>
<th>

`git checkout <branch_name>`
</th>
<td>
Change to a branch
</td>
</tr>
</table>




### D-3) `merge`:


To merge two branches.






<table>
<tr>
<th>

`git merge <branch_name>`
</th>
<td>
Merge a branch to the current branch
</td>
</tr>
<tr>
<th>

`git merge --abort`
</th>
<td>
Abort a merge and try to construct a pre-merge state
</td>
</tr>
<tr>
<th>

`git merge --continue`
</th>
<td>
Continue a merge if there has been a conflict
</td>
</tr>
<tr>
<th>

`git merge <branch_name> --no-ff`
</th>
<td>
Merge without fast-forward
</td>
</tr>
<tr>
<th>

`git merge --strategy=<option> <branch_name>`
</th>
<td>
Merge with a custom strategy
</td>
</tr>
<table>




### D-4) `log`:

Show the commit history.



<table>
<tr>
<th>

`git log`
</th>
<td>
Show the commit history
</td>
</tr>
<tr>
<th>

`git log --oneline`
</th>
<td>
Show the commit history in a single line
</td>
</tr>
<tr>
<th>

`git log --graph`
</th>
<td>
Show the commit history in a graph
</td>
</tr>
<tr>
<th>

`git log --graph --oneline`
</th>
<td>
Show the commit history in a graph and a single line
</td>
</tr>
<tr>
<th>

`git log --pretty=<format>`
</th>
<td>
Show the commit history in a custom format
</td>



<tr>
<th>

`git log <file_directory>`
</th>
<td>
Show the commit history of a file
</td>
</tr>
<tr>
<th>

`git log <branch_name>`
</th>
<td>
Show the commit history of a branch
</td>
</tr>
</table>


### D-5) `tag`:

To create and list tags.




<table>
<tr>
<th>

`git tag`
</th>
<td>
List all tags
</td>
</tr>
<tr>
<th>

`git tag <tag_name>`
</th>
<td>
Create a new tag
</td>
</tr>
<tr>
<th>

`git tag -d <tag_name>`
</th>
<td>
Delete a tag
</td>
</tr>
<tr>
<th>

`git tag -a <tag_name> -m <message>`
</th>
<td>
Create a new annotated tag
</td>
</tr>
<tr>
<th>

`git tag -a <tag_name> -m <message> <commit_SHA>`
</th>
<td>
Create a new annotated tag from a commit
</td>
</tr>
<tr>
<th>

`git tag -a <tag_name> -f <file_path>`
</th>
<td>
Create a new annotated tag from a file
</td>
</tr>
</table>





# E) Sharing and Updating:




### E-1) `fetch`:


To download remote branches.




### E-2) `pull`:


To merge changes from a remote branch.




### E-3) `push`:
To upload changes to a remote branch.





# F) Patching:


### F-1) `revert`:

To revert changes in a new commit.



```bash
git revert <commit_SHA>
```

This will create a new commit with the changes from the old commit, and ask you to input a commit message.



### F-2) `rebase`:

To apply changes from a remote branch, and mix the branches into one branch with the same line.





```bash
git rebase <branch_name>
```







# Graphs:

## 1) `git merge`:


<b>


```
git checkout f
git merge m
git checkout m
git merge f
git log --oneline --graph
```

</b>


```
*   157b734 (HEAD -> m, f) Merge branch 'm' into f
|\
| * d37ff03 m6
| * cfbd014 m5
| * 7aca9e4 m4
* | 528aeb9 f4
* | a8c55fa f3
* | adcfecf f2
* | fe68070 f1
|/
* 35670a9 m3
* 0957f14 m2
* 0e44225 m1
```





## 2) `git merge --squash`:



<b>

```
git checkout f
git merge m --squash
git commit -m "merged"
git checkout m
git merge f
git commit -m "merged"
git log --oneline --graph
```

</b>


```
* c555842 (HEAD -> m) merged
* d37ff03 m6
* cfbd014 m5
* 7aca9e4 m4
* 35670a9 m3
* 0957f14 m2
* 0e44225 m1
```





## 3) `git rebase`:



<b>

```
git checkout f
git rebase m
git checkout m
git rebase f
git log --oneline --graph
```

</b>


```
* 7c00c56 (HEAD -> m, f) f4
* e578bd7 f3
* db42864 f2
* 003f332 f1
* d37ff03 m6
* cfbd014 m5
* 7aca9e4 m4
* 35670a9 m3
* 0957f14 m2
* 0e44225 m1
```












# Questions:

### 1) Explain These Commands:

<b>


```
B)

git clone <repository_URL>
git init


C)

git add .
git add <file_location>
git status

git diff
git diff <commit_SHA> -- <file_path>
git diff topic master
git diff topic..master
git diff topic...master

git commit
git commit -m "message"
git commit -a (--all) -m "message"
git commit --file <file_path>


git restore <file_path>
git restore --staged <file_path>
git restore --source <source SHA> <file_path>

git reset <commit_SHA>

git rm <file_path>


D)

git branch
git branch <branch_name>
git branch -d (--delete) <branch_name>
git branch <branch_name> <commit_SHA>
git branch -m (--move) <old_branch_name> <new_branch_name>
git branch --copy <old_branch_name> <new_branch_name>

git checkout <branch_name>

git merge <branch_name>
git merge --abort
git merge --continue
git merge <branch_name> --no-ff
git merge --strategy=<option> <branch_name>

git log
git log --oneline
git log --graph
git log --graph --oneline
git log --pretty=<format>
git log <file_directory>
git log <branch_name>

git tag
git tag <tag_name>
git tag -d <tag_name>
git tag -a <tag_name> -m <message>
git tag -a <tag_name> -m <message> <commit_SHA>
git tag -a <tag_name> -f <file_path>


E)

git fetch

git pull

git push

git revert <commit_SHA>

git rebase <branch_name>
```

</b>




### 2) What is the differenece between?


<b>

- `reset`, `restore`, `revert`
- `rebase`, `merge`
- `pull`, `push`, `fetch`
</b>






