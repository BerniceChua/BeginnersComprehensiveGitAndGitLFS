# First-Time-Setup Instructions
This the 1st-time setup for beginners.  A lot of these things can be tedious, but once you are done, you don’t need to deal with them again for the most part.  

To be honest, all people who work with `git` can’t remember all the steps, especially those for setting up `git` in a local machine, since this is not something that people often need to deal with.  Most people have to look up guides for these too as reminders, if they don’t interact with them a lot, so don’t feel bad if you are lost.  

I will indicate if something is a 1-time action, or an action that needs to be done per computer, or an action that needs to be done at the beginning of each repo’s creation, or an action that needs to be done once per repo clone.

- 1-time action, as the name indicates, is something that you'll never ever have to deal with again.  
- Once per local machine means that when you are using a different computer that doesn’t have `git` set up yet, you’ll need to do this again.
- Once per repo creation means that this needs to be done if you are creating a repo for the first time ever and it hasn’t existed anywhere else yet.
- Once per clone means that you are working on an existing repo and you are downloading that repo into your local machine for the first time.  

## Table Of Contents:
- [First-Time-Setup Instructions](#first-time-setup-instructions)
  * [Step 0 - Text Editor](#step-0---text-editor-)
    + [Skip this step if](#skip-this-step-if-)
  * [Step 1 - Create an account in the remote repo](#step-1---create-an-account-in-the-remote-repo-)
  * [Step 2 - Downloading & Installing](#step-2---downloading---installing-)
  * [Step 3 - Configuration](#step-3---configuration-)
    + [Step 3.1 - Configuration - Identity:](#step-31---configuration---identity-)
    + [Step 3.2 - Configuration - Text Editor:](#step-32---configuration---text-editor-)
  * [Step 4 - Install `git lfs`:](#step-4---install--git-lfs--)
    + [TO KNOW MORE:](#to-know-more-)
    + [FUN FACT:](#fun-fact-)
  * [The End](#the-end)


## Step 0 - Text Editor:
(Once per local machine.)  
There will be a part of the `git` installation process that will ask for a text editor.  

### Skip this step if:  
If you already have a text editor or if you already know how to use `vim`, then you can skip this step.

What is this for?
There will be parts of the `git` process where you might need to write some short comments.

You can even use the default text application of your computer (gedit for Linux, Notepad for Windows, and whatever it is that Mac uses).

But if you want to use something that has code completion and syntax highlighting, these are some options:
- Notepad++ = https://notepad-plus-plus.org/
* Atom = https://atom.io/
Visual Studio Community = https://visualstudio.microsoft.com/vs/community/
For Linux & Mac users who can’t use Visual Studio Community, here is Visual Studio Code = https://code.visualstudio.com/


## Step 1 - Create an account in the remote repo:
(1-time action)
Create an account in your remote repository of choice.  In this example, since we are game developers, we will use GitLab.  

https://gitlab.com/

NOTE:
If you already have a GitHub account, you can use it to OAUTH an account for GitLab.


## Step 2 - Downloading & Installing:
(Once per local machine.)
Download and install `git bash`:

https://git-scm.com/download/

What is this for?  
This is the client for accessing and using `git`, and for communicating with the remote repo.  Think of it like using the internet.  You need to use a web browser like Firefox or Chrome to access different websites.  

In https://git-scm.com/book/en/v2/Getting-Started-Installing-Git, go to the section of your operating system (Linux or Windows or Mac).  And follow the instructions there.



## Step 3 - Configuration:
(Once per local machine.)  
When installing `git` with `git bash`, follow the instructions.  The default options for everything should be fine.  

https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup has details about what needs to be done.

### Step 3.1 - Configuration - Identity:
(Once per local machine.)  
`git` will ask for your identity, which is your name and your email address.  This should match the name and email address that you’ve provided to sign up for the remote repo, so that you can link this account later.  

### Step 3.2 - Configuration - Text Editor:
(Once per local machine.)
At 1 point, it will ask you what text editor you wish to use.  I think that `vim` is very powerful, but it takes some getting used to.  

This is where Step 0 comes in.  
You also have the option of using other text editors.  Select a text editor you’d like to use with Git. Use the drop-down menu to select Notepad++ (or whichever text editor you prefer) and click Next.

This is not set in stone, and you have the option to change the text editor later (see instructions here: https://docs.github.com/en/github/using-git/associating-text-editors-with-git )

In the future, if you want to learn how to use vim, here are some resources:
https://www.freecodecamp.org/news/vim-isnt-that-scary-here-are-5-free-resources-you-can-use-to-learn-it-ab78f5726f8d/


## Step 4 - Install `git lfs`:
`git lfs` stands for “git Large File System”.  This is important for projects that work with a lot of large files.  For `git` (and especially GitHub), large files means they are files that are larger than 100MB (Megabytes).  

To install `git lfs`, follow the instructions here: 
https://git-lfs.github.com/

### TO KNOW MORE:
A more detailed explanation of the entire process is here: 
https://thoughtbot.com/blog/how-to-git-with-unity

### FUN FACT:
The capitalization of “B” in “MB” or “KB” or “GB” or “TB” for file-sizes is important.  If the “B” is capitalized, it means “Bytes”; when the “b” is small, it means “bits”.  Bytes are bigger than bits, because 1 Byte = 8 bits.  (This is where the phrase 8-bit, etc. comes from!)  So when something is abbreviated as Mb & Kb, that’s smaller because it means Megabit & Kilobit, respectively.

## The End


| [Back: Introduction](/tutorials/INTRODUCTION.md) | [Table Of Contents](tutorials/TABLE_OF_CONTENTS.md) | [Next: Your First `git` Repo](/tutorials/Your_First_git_Repo.md) |
| :-: | :-: | :-: |
