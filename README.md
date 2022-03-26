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
</table>











