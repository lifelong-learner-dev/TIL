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

<br>

>> * Switched to branch '...' → <br> You can confirm that the branch you've moved to has an asterisk (*) next to its name.

<br>

>> * Create a new branch and switch to it immediately
```markdown
git checkout -b new_branch_name
```
>> * If you switch without creating it first, 
     <br> you'll get a path error (not found).

<br>

***

<br>

# Merge Scenarios

> cake.txt
>> Mara mint chocolate dark brown sugar Tanghulu cake

```markdown
git add .
git commit -m "Recipe"
git checkout -b secret
```
>> Created cake.txt, committed its content, and then created the 'secret' branch based on that commit.

```markdown
git checkout -b secret2
```
>> The reason for switching branches is to isolate new changes

<br>

> cake.txt
>> **contents** : Spicy hot mara mint chocolate dark brown sugar Tanghulu banh mi sandwich
```markdown 
git add .
git commit -m "Recipe2"
git checkout secret
```
<br>

```markdown
git branch -d secret2
```
>> Forced deletion since it wasn't merged

<br>

```markdown
git checkout -b secret3
```
> cake.txt
>> **contents** : Mara mint chocolate dark brown sugar Tanghulu cake
Mara mint chocolate dark brown sugar Tanghulu macaron


```markdown 
git add .
git commit -m "Recipe3"
git checkout secret 
```
>> Move back to the original branch

<br>

```markdown
git merge secret3 
```
>> Merge the branch you want to combine

<br>

```markdown
git branch -d secret3 
```
>> No need for forced deletion since it's merged
```markdown
git merge
```
```markdown
git checkout {branch_to_receive_merge}
git merge {branch_to_merge}
```

<br>

***

<br>

# Conflict Scenarios

```markdown
git branch cat
git branch dog
```
> Currently branching out from the existing branch into 'cat' and 'dog'

<br>

```markdown
git checkout dog
```
> pet.txt
>> Dog

<br>

```markdown
git add .
git commit -m "Dog"
git checkout cat
```
>> In the 'cat' version, pet.txt doesn't exist,
   <br> so it's treated as nonexistent

<br>

> pet.txt
>> Cat

<br>

```markdown
git add .
git commit -m "Cat"
git merge dog 
```
> Merge the 'dog' branch into the 'cat' branch
```markdown
git merge --abort 
```
> Abort the merge
>> **Current Changes** : Apply changes from the currently checked out branch.
<br>

>> **Accept Incoming Changes** : Apply changes from the branch you want to merge into (the branch you're merging into).
<br>

>> **Accept Both Changes** : Apply both sets of changes.

```markdown
git add . 
```
>> After deciding on the changes

```markdown
git commit -m "Merge-related message"
```
>> **Please note that the comments explain the actions and options associated with each Git command.**

<br>

***

<br>


# git remote

> A feature that connects a remotely created repository on GitHub with your local repository.

```markdown
git remote -v
``` 
>> List of currently connected remote repositories

```markdown
git remote add origin <link to the remote repository to be added>
```
```markdown
ex) 
git remote add origin https://github.com/username/project(repository)name
```
```markdown
git remote -v
```
<br>

> Two scenarios:
>> 1. Typos in the remote repository name like 'orgin', 'orign', 'origi'
>>> * Simply re-enter it as 'origin'

<br>

```markdown
git remote remove <repository name>
```
```markdown
git remote remove origin
```
>> 2. Correct 'origin' but an issue with the URL
```markdown
git remote remove origin 
```
>>> * then re-enter it

>> **The reason for removing or reconfiguring is** :
>>> error: remote origin already exists.

```markdown
git remote set-url origin ...
```
>> Execute the 'set-url' command related to remote, <br>
 specifying 'origin' as the target and assigning a new URL.

<br>

> 1
```markdown
git branch -M main
git push -u origin main
```
> 2
```markdown
git push -u origin master
```

<br>

> Local to Remote
>> Adding (registering) a remote repository (on the internet) -> origin -> https://...(URL).git

<br>

```markdown 
git remote add origin https://github.com/username/project(repository)name.git
```
>>> Changing the branch name from 'master' to 'main'

```markdown
git branch -M main 
```
>> Pushing (uploading) the local version to remote
```markdown
git push -u origin main 
```
>> Pushing the 'main' branch to the 'origin' remote repository

<br>

> Please note that the branch name might be 'main' or 'master' <br> depending on the branching convention used in your project. <br> The above examples demonstrate both cases.

<br>

***

<br>

# Remote Repository Functions
 > Remote Scenarios
>>Commits have diverged between local and remote.
```markdown
git pull origin <branch name>
```

<br>


> Update data of a specific branch in the 'origin' repository (GitHub repository)
```markdown
git pull origin master
git pull origin main
```
>> Use push to update the remote repository and pull to retrieve the updated content.

>> You can specify a particular branch name, such as 'main' or 'master,' to save and retrieve data, making it similar to a drive folder.

>> You need to fetch an existing remote repository to the local (not creating a new one with git init). 
>>> * Instead of using pull, use clone initially to replicate the existing data and then use pull to fetch changing data.
```markdown
git clone <repository URL>
```
>> Can be obtained regardless of editing permissions, as long as it is a public repository
git clone https://github.com/username/project(repository)name

>> Possible for both public and private repositories,
<br> but changes in the remote repository won't be reflected.

<br>

***

<br>

# .gitignore

> Specifies files that should not be included in git add.

> When you specify a filename or folder path, that file/folder/path will no longer be detected (staged) by git add. <br>

> Create a file named .gitignore in the base folder, and enter the patterns to be excluded in that file.
```markdown
 .gitignore
```
>> Comments are allowed!

> ex)
secret_password.txt
>> Enter the exact file/path name

> home* 
>> * for patterns at the start, middle, or end

> *home* 
>> Similar to regular expressions (not an exact match)

> *.jpg
>> passwords/