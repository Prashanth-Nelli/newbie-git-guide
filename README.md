##Newbie-Git-Guide

A newbie Git guide.

###Git Basics :-

#### ``` 1. Git Configuration :-```

##### ``` Configuring User Details Git :- ```

```
    1. System level     :-  git config --system user.name gituser
    2. User level       :-  git config --global user.name gituser
    3. Repository level :-  git config user.name gituser
```
##### ``` Configuring Editor for writing Commit Messages :- ```

```
    git config --global core.editor 'subl -n -w'
    git config --global core.editor 'vim -w' 
    git config --global core.editor 'atom -w'
```
##### ``` Settings :- ```
``` 
    1. Checking Your Settings :-
```
```
            git config --list
        
output:-    user.name=git user
```
```
    2. Checking Settings by Key :-
```
```
            git config {key}
```

#### ```2. Getting A Git Repo :- ```
```
    1. Converting An Existing Repo Into Git Repo :-Goto that Root Directory and run the following command
        git init.
    2. Cloning an Existing Repository :-
        git clone {repo link}
```
#### ```3. Staging Modified Files :-```
```
    git add {filname(s)}
```
#### ```4. Unstaging Staged Files :-```
```
    git HEAD reset {filname(s)}
```
#### ```5. Seeing the changes in Unstaged Files :-```
```
    git diff
```
#### ```6. Seeing the changes in Staged Files :-```
```
    git diff --staged
```
#### ```7. Commiting Staged Files :-```
```
     git commit -m "{commit message}"

Eg:-
    git commit -m "Intial Commit"    
```
#### ```8. Seeing File Changes introduced due to Commits :-```
```
    git show {commit hash}

Eg:-
    git show 085b24d749c5376b7e022dbc83b6a05d0783bb97
```
#### ```9. Changing Commit message of previous Commits :-```
```  
    1. Changing the Commit Message of the latest commit on the branch
         
       git commit --amend -m "Modified Commit Message"
    
    2. Changing the Commit Message of the commits other than latest commit

       git rebase -i <commit-to-change>~

       This will fire up an editor. Replace pick with edit on the correct commit entry, save and exit. Then:

       git commit --amend -m "New commit message"
       
       git rebase --continue
```
