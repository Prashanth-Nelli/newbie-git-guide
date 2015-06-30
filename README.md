### Newbie-Git-Guide

A newbie Git guide.

####Git Basics :-

#####Git Configuration :-

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
