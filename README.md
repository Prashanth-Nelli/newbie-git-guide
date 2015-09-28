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

####```10. Removing Files :-```

```

1. Removing Files and adding them to staging area

   git rm filename

2. Removing a staged file

   git rm filename -f

3. Making a file untracked but keeping it in hard drive.

   git rm --cached filename

```

####```11. Moving Files :-```

```
1. It will move one file to another another file and it will add it to
   staging area.

    git mv filename filename2

```

####```12. Viewing the Commit History :-```

```
1. git log

--> it will lists the commits made in the repository.

2. git log -p -n

--> It will show the difference introduced in each commit till lat "n" commits.

3. git log --stat

--> It will show abbreviated stats for each commit.

4. git log --pretty=oneline

--> It will display commit SHA and commit message.

5. git log --pretty=format:"%h - %an, %ar : %s"

--> It will display custom log messages.

Options for git log --pretty=format :-

    Option  Description of Output
    %H      Commit hash

    %h      Abbreviated commit hash

    %T      Tree hash

    %t      Abbreviated tree hash

    %P      Parent hashes

    %p      Abbreviated parent hashes

    %an     Author name

    %ae     Author email

    %ad     Author date (format respects the --date=option)

    %ar     Author date, relative

    %cn     Committer name

    %ce     Committer email

    %cd     Committer date

    %cr     Committer date, relative

    %s      Subject

Common options to git log :-

    -p

        Show the patch introduced with each commit.

    --stat

        Show statistics for files modified in each commit.

    --shortstat

        Display only the changed/insertions/deletions line from the --stat command.

    --name-only

        Show the list of files modified after the commit information.

    --name-status

        Show the list of files affected with added/modified/deleted information as well.

    --abbrev-commit

        Show only the first few characters of the SHA-1 checksum instead of all 40.

    --relative-date

        Display the date in a relative format (for example, “2 weeks ago”) instead of using the full date format.

    --graph

        Display an ASCII graph of the branch and merge history beside the log output.

    --pretty

        Show commits in an alternate format. Options include oneline, short, full, fuller, and format (where you specify your own format).

Options to limit the output of git log :-

    -(n)

    Show only the last n commits

    --since, --after

    Limit the commits to those made after the specified date.

    --until, --before

    Limit the commits to those made before the specified date.

    --author

    Only show commits in which the author entry matches the specified string.

    --committer

    Only show commits in which the committer entry matches the specified string.

    --grep

    Only show commits with a commit message containing the string

    -S

    Only show commits adding or removing code matching the string

```