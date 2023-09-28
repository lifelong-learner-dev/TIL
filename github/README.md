# 1. Let's turn the current folder into a Git repository.
```markdown
git init
```
* For those who have set hidden folders to be visible, you will see the .git folder.
## 1-1. How to make the current folder not a Git repository.
```markdown 
rm -rf .git
```
1. **rm** : remove, it will remove -> .git (usually hidden)

2. **-rf** : 
   1. > -r, the 'rm' command can't delete folders by default; <br>
     -r is used to delete folders, 
   2. > -f is a force command to ensure deletion.

*** 
<br>

# 2. Command to stage (temporarily store) the currently changed files.

```markdown
git add {path to the file you want to add}
```
* You can use 'git add *' or 'git add .' to stage all the changes made so far.
> **What does Git use as a basis for detecting changes?**
>> (1) It uses the changes made after 'git init' as a basis. <br>
<br>
>> (2) It is based on individual files (it doesn't detect changes in folders alone).
```markdown
git status
```
* Check the files currently staged (temporarily stored).<br>
<br>
## 2-1. Reset the current staging list.
```markdown
git reset
``` 
<br>

***

<br>

# 3. The process of finalizing the changes made so far.
```markdown
git commit
```
> **Issues when using this command alone :**
>> 1. If your personal information is not set, committing is not possible.
<br><br>
>> 2. It asks for the name and email of the person committing. 
<br><br>
>> 3. Is your information set correctly? (Author identity unknown)
```markdown
git config --list
```
* user.name={Your name (recommended: GitHub username)}
<br>
<br>
* user.email={Your email (recommended: the email used when signing up for GitHub)}

```markdown
git config --global user.name "..."
```
```markdown
git config --global user.email "..."
```
* **configuration** : settings <br><br>
* **/ --global** : applies my settings globally no matter which folder I'm in <br><br>
* **user (user).email (email attribute) "..."** : 
  * Typically, you would put the email you used when signing up for GitHub

> ## 3-1. If you just use 'git commit,' it goes into the text editor to write a commit message.
>> * To exit the text editor: press esc -> type : -> press q -> hit enter <br><br>
>> * Write the commit message <br><br>
>> * i (-- INSERT -- will appear) -> esc -> : -> wq -> enter <br>

<br>

> ## 3-2. How to write commands directly in Git Bash
```markdown
git commit -m "Commit message"
```

<br>

> ## 3-3. Check if the changes were applied successfully after committing.
```markdown
git status
```
>>  * Check if there are no remaining files in the staging area and if the commit was successful.

```markdown
git log
```
>> * View the commit history up to this point. <br>
If it gets too long, you will need to scroll using the arrow keys. 
<br><br>
>> * Press 'q' to exit the log.


<br> 

> ## 3-4. Modify the content of the previous commit.

```markdown
git commit --amend
```

>> * It will open the text editor again, allowing you to edit any mistakes in the commit message.
<br>

<br>

> ## 3-5. Go back to a previous commit.
```markdown
git log
```

>> * Find the commit address you want to go back to : 
     <br> commit ~~~
```markdown
git checkout {commit address}
```
>> * HEAD -> The current working position (commit) has an option to determine it.
<br><br> 
>> * You can change it to a specific commit address to go back to.

<br><br>

***

<br>

# 4. git branch

- The trunk of the tree. 
  <br>A collection of different versions branching out.
<br><br>

- Gives names to commits, 
  <br> and from that commit onward, 
  <br> they are considered separate versions.

<br>

> ## Create a branch
```markdown
git branch branch_name
```
>> * Example: git branch develop

<br>

> ## Check the list of branches
```markdown
git branch
```
>> * Helps manage the current version by task 
     <br> or feature unit for workers or teams.

<br>

> ## Delete a branch
```markdown
git branch -d branch_name 
```
>> * Regular deletion (after merging)
```markdown
git branch -D branch_name 
```
>> * Force deletion (if not merged)



```markdown 
git checkout
```
>> * How to move between 'develop' branch and 'main' branch.