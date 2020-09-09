| [Back: First-Time-Setup Instructions](/tutorials/First-Time-Setup_Instructions.md) | [Main Table Of Contents](/tutorials/TABLE_OF_CONTENTS.md) | [Next: Interacting With `git`, And How To Contribute Your Work To The Repo](/tutorials/git_Interactions.md) |
| :-: | :-: | :-: |


# Your First `git` Repo
More likely than not, you will join an existing remote repository.  This is done with something called "cloning" or "to clone", which makes a local copy to your computer.  To do so, follow the instructions in [A: Linking an existing remote repo to your local machine](#a-linking-an-existing-remote-repo-to-your-local-machine).  

If you want instructions on how to to start your own git repo, go to [B: Creating your own `git` repo from scratch](#to-do-b-how-to-create-your-own-git-repo-from-scratch).

## Table Of Contents:
- [Your First `git` Repo](#your-first-git-repo)
  * [A: Linking an existing remote repo to your local machine](#a-linking-an-existing-remote-repo-to-your-local-machine)
    + [Step 1 - How To Open Git Bash](#step-1---how-to-open-git-bash)
    + [Step 2 - Using the command line to go to the directory you want](#step-2---using-the-command-line-to-go-to-the-directory-you-want)
      - [PRO-TIP 1](#pro-tip-1)
      - [PRO-TIP 2](#pro-tip-2)
    + [Step 3 - Clone the project from the remote repo](#step-3---clone-the-project-from-the-remote-repo)
      - [Step 3.1 - the “copy” part](#step-31---the-copy-part)
        * [GitLab Version](#gitlab-version)
        * [(TO DO) GitHub Version](#to-do-github-version)
      - [Step 3.2 - the “paste” part](#step-32---the-paste-part)
      - [FUN FACT](#fun-fact)
      - [CHECK THAT EVERYTHING IS THERE AND EVERYTHING IS OK](#check-that-everything-is-there-and-everything-is-ok)
    + [NOTE](#note)
  * [(TO DO) B: How to create your own `git` repo from scratch](#to-do-b-how-to-create-your-own-git-repo-from-scratch)
  * [The End](#the-end)


## A: Linking an existing remote repo to your local machine:
(Once per repo, Once per local machine, Once per clone.)  
To join an already-existing project, you will need to make a copy of the project from the remote repo.

### Step 1 - How To Open Git Bash
(Once per repo, Once per local machine, Once per clone.)  
In your computer, decide where you want to store the project.  Once you have decided where to save it, open up `git bash`.  It’s the icon that looks like this:
![GitBash Icon](/images/GitBashIconCapture.PNG?raw=true "GitBash Icon")

### Step 2 - Using the command line to go to the directory you want:
(Once per repo, Once per local machine, Once per clone.)  
In my example, I'm going to store things inside a directory called "Unity-Stuff"

So I will type:
```bash
cd ~/Unity-Stuff/
```
![Going To The Directory](/images/using_git_tutorial_01.PNG?raw=true "Put in Unity-Stuff/ directory")  

What do each of these things mean?  
| Command | Meaning|
| :-: | :- |
| `cd` | the keyword to change directories |
| `~` | The squiggly in front of the backslash (`~`) just means that the `Unity-Stuff` directory is in my home folder.  It’s a shortcut that means:
`C:\Users\[your username]\` in Windows, or `/home/[your username]/` in Ubuntu. |

The last part will be different depending on where you want to store your local repo.  

In this example, `Unity-Stuff` is a directory that I have where I keep all my Unity game dev work by default.  If you are using a different directory, like `Documents` or something, then your version will be:
```bash
cd ~/Documents/
```
![Going To The Directory](/images/using_git_tutorial_02-saveToDocuments.PNG?raw=true "Put in Documents/ directory")

#### PRO-TIP 1:
To make sure that the directory exists, type the name part of the way, then press the `Tab` key of your keyboard.  This will help you do auto-complete! ^_^  This is called “tab-completion”.  If you have a bunch of things with the same name, `git bash` will show you the options that you have.


#### PRO-TIP 2:
You can check which directory you are at by reading the yellow words.  
![Going To The Directory](/images/using_git_tutorial_03-yellowWords.PNG?raw=true "Put in Documents/ directory")

If the yellow words are too long that it gets cut off at the end, type `pwd` then press enter.  This will display what directory you are at.  `pwd` is the keyword that means “print working directory”.  
![How to use `pwd`](/images/using_git_tutorial_04-usingpwdPNG.PNG?raw=true "How to use `pwd`")

### Step 3 - Clone the project from the remote repo:
(Once per repo, Once per local machine, Once per clone.)  
Now that you are in the directory that you want to save the project in, use your web browser to go to the webpage of the remote repo.  

You will usually be provided with a direct link for this, usually because you will be invited as contributors to this repo.  You will know this is the case, because the people who manage the repo will ask you for your email address or your username in either GitHub/GitLab.  

When you are in the webpage of the remote repo, look for this:  
![Clone Button With Arrow](/images/using_git_tutorial_05-cloneButtonWithArrow.PNG?raw=true "Clone Button With Arrow")


#### Step 3.1 - the "copy" part:
(Once per repo, Once per local machine, Once per clone.)  
Click on the button that says "Clone".  

##### GitLab Version:
In GitLab, it looks like this:
![Clone Button With Arrow](/images/using_git_tutorial_05-cloneButtonWithArrow.PNG?raw=true "Clone Button With Arrow")

##### (TO DO) GitHub Version:
(TO DO: add the screenshot of the GitHub version.)

When you click on that button, a dropdown menu appears.  For our purposes today, please click on the button beside the `Clone with HTTPS` version.  (TO DO: make a future tutorial for the SSH version.)  
![Going To The Directory](/images/using_git_tutorial_06-clickOnCloneButtonWithArrow.PNG?raw=true "Arrow pointing to the `Clone with HTTPS` button")  
This button copies that string of text automatically for you.

#### Step 3.2 - the “paste” part:
(Once per repo, Once per local machine, Once per clone.)  
Next, in your `git bash`, type:  `git lfs clone ` (remember to put a space after the word "clone").  Then right click on the space next to it to make a dropdown menu come down.  Look for "Paste", then click on that.  (An alternate way to paste is the keyboard shortcut `Shift`+`Insert`.)  

When that string of text is pasted, hit `Enter` on your keyboard.  This completes the `git lfs clone` command.

In full, it looks like this:  
```bash
git lfs clone [URL_of_repo]
```

If everything is OK, the message will look like this:  
![Going To The Directory](/images/git-clone.png?raw=true "git clone")  
![Going To The Directory](/images/git-lfs-example_50409937-fbf37680-0830-11e9-8b88-845682b626e9.png?raw=true "git lfs clone")  


#### FUN FACT:
Normally, people type `git clone ` instead of `git lfs clone `.  But we are doing it this way, because game dev repos usually have lots of large files, so it’s just faster to use the LFS version.  (See here for reference: https://blog.developer.atlassian.com/git-lfs-12-clone-faster/)

CONGRATULATIONS!  You have just cloned your first repo!  Now you have a copy of the project in your local machine.  

#### CHECK THAT EVERYTHING IS THERE AND EVERYTHING IS OK:
To check that everything is there, go into the directory that you just cloned.  The directory's name is the same as the repo's name.  

You do this by typing in the command line:
```bash
cd [directory name]
```
Remember to put a space between `cd` and the directory name.  Then hit `Enter` on your keyboard.

It should appear this way:
![Going To The Directory](/images/use_cd_to_change_directory.PNG?raw=true "using `cd` to change directory")  

You are now inside the directory of the repo that you just cloned! ^-^

Take note that this has additional words, like "Master" (in cyan/light blue) and things like that.  The cyan/light blue words say what branch this git repo is currently on.  If a directory doesn't have those cyan/light blue words between parentheses, it means that the directory is not being tracked by git.  
![Going To The Directory](/images/difference_between_git_directory_and_no-git.PNG?raw=true "the cyan/light blue words say what branch this git repo is currently on.")  

If you see these, then it means that the repo has been downloaded and it has git initialized.  You can also check by using your OS's GUI (the usual way that you look for directories and files).

A directory that's initialized with git will have a new directory appears called `.git`, which has all the data related to version control with `git`.  

The next thing to do is type:
```bash
git lfs install
```
To make sure that LFS is indeed initialized.

### NOTE:
Anybody can clone any repo that is publicly available.  If a repo is private, you will need to be given access to it, in order to even see that it exists.  If you try to access a private repo with its URL, GitHub or GitLab will show a “404 - not found” error message.  If a repo is public but you are not explicitly given an email, you can clone the repo, but any work that you'd like to submit would need approval from the people who manage the repo.  


## (TO DO) B: How to create your own `git` repo from scratch
(Once for each new repo.)  
(TO DO: create this section in the future.)


## The End


| [Back: First-Time-Setup Instructions](/tutorials/First-Time-Setup_Instructions.md) | [Table Of Contents](/tutorials/TABLE_OF_CONTENTS.md) | [Next: Interacting With `git`, And How To Contribute Your Work To The Repo](/tutorials/git_Interactions.md) |
| :-: | :-: | :-: |
