# Interacting With `git`, And How To Contribute Your Work To The Repo
To interact with `git`, it is important to make sure that you are in the directory of the repo.  Any directory that has a `.git` folder is a directory that is being version-controlled by `git`.

PRO-TIP:  
If you are ever confused by something in git, you can type `git help [command]` then hit enter.  It will bring up an explanation.  https://git-scm.com/book/en/v2/Getting-Started-Getting-Help


## Table Of Contents:
- [Interacting With `git`, And How To Contribute Your Work To The Repo](#interacting-with--git---and-how-to-contribute-your-work-to-the-repo)
  * [Step 1 - Go Into Your Local Repo:](#step-1---go-into-your-local-repo-)
  * [Step 2 - Make Sure That You Are Working Out Of A Branch:](#step-2---make-sure-that-you-are-working-out-of-a-branch-)
      - [PRO-TIP 1:](#pro-tip-1-)
      - [PRO-TIP 2:](#pro-tip-2-)
      - [PRO-TIP 3:](#pro-tip-3-)
      - [PRO-TIP 4:](#pro-tip-4-)
      - [PRO-TIP 5:](#pro-tip-5-)
      - [NOTE 1:](#note-1-)
      - [NOTE 2:](#note-2-)
  * [Step 3 - Do Your Work As You Usually Would](#step-3---do-your-work-as-you-usually-would)
  * [Step 4 - Backing up files LOCALLY](#step-4---backing-up-files-locally)
    + [Step 4.1 - `git add`](#step-41----git-add-)
    + [Step 4.2 - `git commit`](#step-42----git-commit-)
      - [NOTE 1:](#note-1--1)
      - [NOTE 2:](#note-2--1)
      - [NOTE 3:](#note-3-)
      - [PRO-TIP:](#pro-tip-)
      - [FUN FACT:](#fun-fact-)
    + [Step 4.3 - repeat as needed](#step-43---repeat-as-needed)
  * [Step 5 - Uploading to the remote repo, to back up files and share it with the team.](#step-5---uploading-to-the-remote-repo--to-back-up-files-and-share-it-with-the-team)
    + [Step 5.1 - Precaution: Check For Changes In The Remote Repo](#step-51---precaution--check-for-changes-in-the-remote-repo)
      - [PRO-TIP:](#pro-tip--1)
      - [Step 5.1.1 - If everything goes well:](#step-511---if-everything-goes-well-)
      - [(TO DO) Step 5.1.2](#-to-do--step-512)
    + [Step 5.2 - Pushing your changes to the remote repo](#step-52---pushing-your-changes-to-the-remote-repo)
    + [Step 5.3 - In the remote repo’s website, make a `pull request` / `merge request`](#step-53---in-the-remote-repo-s-website--make-a--pull-request-----merge-request-)
  * [NOTE:](#note-)
- [PRACTICING BY YOURSELF](#practicing-by-yourself)
  * [With This Repo](#with-this-repo)
  * [With Other Sources](#with-other-sources)
    + [Interactive Online Browser-Based Tools](#interactive-online-browser-based-tools)
  * [The End](#the-end)


## Step 1 - Go Into Your Local Repo:
Enter the directory where your git project is.  
You do this by typing in the command line:  
```bash
cd [directory name]
```
Remember to put a space between `cd` and the directory name.  Then hit `Enter` on your keyboard.

It should appear this way:
[screenshot]

## Step 2 - Make Sure That You Are Working Out Of A Branch:
It is very important not to make any changes directly in the `master` branch, or else it will cause conflicts and errors for the project or for the rest of the team who is working together on this repo.

To make a new branch, type in the command line:
```bash
git checkout -b [name of your branch]
```
Then hit `Enter` on your keyboard.

You will notice that the cyan/light blue words in the parentheses have changed from `Master` to the name of your current branch that you are on.  This means that you have moved from the `master` branch to this branch.
[screenshot]

#### PRO-TIP 1:
Always check the cyan/light blue words in the parentheses to make sure which branch you are on.

#### PRO-TIP 2:
If you want to check what branches exist in your local repo, in the command line, type `git branch`
This will show a list of branches in your local machine.  The branch that you are on has an asterisk in front of its name.
[screenshot]

#### PRO-TIP 3:
Branch names cannot contain spaces.

#### PRO-TIP 4:
Remember our friend “tab-completion”?  It works for these `git` commands too! ^-^

#### PRO-TIP 5:
If you are ever confused by something in git, you can type `git help [command]` then hit enter.  It will bring up an explanation.  https://git-scm.com/book/en/v2/Getting-Started-Getting-Help

#### NOTE 1:
How do I name my branch?
The general rule of thumb is that the branch describes what the work is doing.  The important thing is that the branch names are understandable when anyone reads it, so they know exactly what is happening in it.  But aside from that, it really depends on the team that you are working with.  The second-most-important thing about naming conventions is that it is consistent with everything else in the project.

There are 3 styles of branching or branch-naming that I’ve seen commonly done (but there are probably others), and they are:
feature branch = a branch for each new feature, and named for each feature (usually in larger, long term projects.
team-mate branch = a branch for each team-mate, and named for each team-mate (usually in smaller projects, like game jams).
combination of both = the branch name has the team-mate’s name, followed by the name of the feature they are working on.

Honestly, a lot of the details of these things are opinions.  As long as a branch name is understandable and consistent with the team’s naming conventions, then it’s OK.

#### NOTE 2:
When is it time to make a new branch?  For certain, it’s when newly-cloning a repo, just to make sure that the `master` branch will not get messed up.  But aside from that, it’s like the naming conventions.  It depends on the team, so it’s important to consult your team and follow the style-guide if one exists.


## Step 3 - Do Your Work As You Usually Would
After Step 2 and before Step 4, you don’t need to make any changes to your workflow.

## Step 4 - Backing up files LOCALLY
When your work is in a good place, and it’s a good time to save, now is probably a good time to add your work to version control.  

If you want to see what files have been changed, type `git status` in the command line.
[screenshot of git status]

### Step 4.1 - `git add`
To “stage” or to prepare files for version-control, type in the command line:
```bash
git add [name of the file to add]
```
This is for each file that needs to be added.  
[screenshot]

To `add` all files in the current directory, it is:
```bash
git add .
```
(that last character is a period or dot.)  
[screenshot]

To `add` a directory:
```bash
git add [directory name/]
```
(that’s a period or dot.)  
[screenshot]

To `add` ALL changed files:
```bash
git add -A
```
[screenshot]  
Although if a lot of changes have been made, it’s better not to do this unless all the changes are related, or else your `commit` message will be very long.

### Step 4.2 - `git commit`
After running `git add`, this is the part that backs up your work on your  local machine.  

To do this, type in the command line:  
```bash
git commit -m “[Your commit message.]”
```

Wherein:  
| Command | Meaning |  
| :---: | :---: |  
| `git commit` | the command that makes the backup |  
| `-m` | the flag that says make a commit message.  This is important, because it’s for describing what work was done.  It’s for labelling the “snapshot”. |  
| `“[Your commit message.]”` | the description of what changes were made. |  

[screenshot]

#### NOTE 1:
Each `git commit` can contain multiple `git adds`, as long as they are related or similar.

#### NOTE 2:
If `git commit` is written WITHOUT `-m “[Your commit message.]”`, `git bash` will look for the default text editor that you installed, so that a commit message can be written.  All commits need messages.  (This is why `git bash` asked for a default text editor during the first-time-setup.)  

#### NOTE 3:
The convention for writing commit messages is an imperative sentence.  
Examples:  
* "Revert the last commit, which broke the build.”
* “Corrected typo in NPC’s dialogue.”
* “Increase border widths for game over UI pane.”  
* “Change lighting to baked, to solve framerate drops.”
* “Replace 3D model of player from prototype to our customized one.”
* “Add code to make objects invisible if it’s between the camera and the player.”

Read these for explanations and for more examples:  
* https://www.freecodecamp.org/news/writing-good-commit-messages-a-practical-guide/
* https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53

#### PRO-TIP:
Commit messages need to be clear, so that referring to it later (either manually or with `git log`, more on this later), people can find things easily, and know exactly what each commit has changed.

#### FUN FACT:
When `git` saves changes, it doesn’t actually save the entire document.  It just saves a “differential” or a “diff”, which is the snapshot of what got changed.  For example, the “diff” of when a file is first created is the entire file; the diff of an edit to that file is just the changes to the file.  This is how `git` can back up lots of things while still allowing users to go back and forth in its timeline, and not take up too much space.  


### Step 4.3 - repeat as needed
Keep doing steps 4.1 and 4.2 for each new feature


## Step 5 - Uploading to the remote repo, to back up files and share it with the team.
When you are satisfied enough with your work to share it with everyone in the team, it is time to push changes to the remote repo.  

### Step 5.1 - Precaution: Check For Changes In The Remote Repo
As a precaution, it’s important to get changes from the remote repo first, before pushing your changes.  To get changes from the remote repo, type in the command line:
```bahs
git pull origin master
```
Then hit the `Enter` key on your keyboard.  
[screenshot]

Explanation:  
* `git pull` is the command that pulls changes from the remote repo.  
* `origin` is the shortcut for the URL of the remote repo.  
* `master` is the name of the main branch.  It could be called something else, but the default is `master`.  

#### PRO-TIP:
To check what is set as the remote repo, type in the command line:
```bash
git remote -v
```
Then hit `Enter` on your keyboard.

#### Step 5.1.1 - If everything goes well:
If there is nothing to update, it will look like this:  
`nothing to update`
[screenshot]

If there are changes, it will look like this:  
[screenshot]

But there’s sometimes a case where `git bash` will bring up the default text editor after pulling from the remote repo.  This is the other reason why `git bash` asks for a default text editor.  The reason for this is for writing a comment about what is being merged.  Usually a message like `Sync with remote repo.` will suffice, unless major changes need to be made.  

#### (TO DO) Step 5.1.2
To Do: complete Step 5.1.2

### Step 5.2 - Pushing your changes to the remote repo
This step actually prepares the changes to be shared to the remote repo.  

To “stage” or to prepare files for version-control, type in the command line:
```bash
git push origin [branch name]
```
This is for each file that needs to be added.
[screenshot]


### Step 5.3 - In the remote repo’s website, make a `pull request` / `merge request`
In the remote repo’s website, 
Step


## NOTE:
Why are there so many steps? Even for just for backing up a file locally?  Then there are even so many steps for backing up to the server??  

The first time I used `git`, I was also confused by this.  But I learned that there are good reasons for all this.  It’s mainly to ensure that anything that’s done is reversible if mistakes are caught early, and easily fixable.

An easy way to think of this entire process is the same as putting stuff into a delivery van.

`git add` is the equivalent of putting stuff into a box.  

`git commit` is like labelling a box and marking it for putting into the delivery van; saying that it is ready for delivery.  

`git push` is like putting those labelled boxes into the delivery van

Going to the remote repo and making the pull request is the equivalent of sending stuff to their destination.

You can use this analogy to explain `git` to others, just give credit to me for where you found this idea.  


# PRACTICING BY YOURSELF
Practice more to get comfortable using git.
## With This Repo
If you want to practice more by yourself, feel free to clone this repo and mess around with making new branches, switching branches, making changes to files or adding files, making adds and commits, making pull requests, and anything else.  

## With Other Sources
### Interactive Online Browser-Based Tools
- “Learn git Branching”  
  - https://learngitbranching.js.org/

- Katacoda  
  - https://www.katacoda.com/courses/git & https://www.katacoda.com/courses/git/playground
  - Free to make an account, and free to use

- Git Exercises
  - https://gitexercises.fracz.com/

- Visualizing git
  - http://git-school.github.io/visualizing-git/
  - Explore how Git commands affect the structure of a repository within your web browser with a free explore mode, and some constructed scenarios.


## The End


| [Back: Your First `git` Repo](/tutorials/Your_First_git_Repo.md) |
| :-: |

<p align="justify">
| [Table Of Contents](tutorials/TABLE_OF_CONTENTS.md) |
| :-: |
</p>


<p align="right">
| [Next: Glossary](/tutorials/GLOSSARY.md) |
| :-: |
</p>
