| [Back: Main Table Of Contents](/tutorials/TABLE_OF_CONTENTS.md) | [Next: First-Time-Setup Instructions](/tutorials/First-Time-Setup_Instructions.md) |
| :-: | :-: |

# Introduction:
This is about setting up `git` for first-time-ever users.  `git` is a tool used for version control.  

But first, what is version control?  In the past, I made a blog post about it.  Please read it here: http://bernicechua.github.io/blog/git  

So why would you want version control?  The TL;DR of that blogpost is:
- It allows people to create backups of their work both locally and on a remote server.
- It allows multiple people to collaborate on the same project at the same time without over-writing their team-mate's work or denying access to other team mates.

The version control tool and process that I'll talk about today is called `git`.  

There are 2 parts:  
Using version control with `git` actually has 2 parts to it.  That's what I meant when I said "both locally and in a remote server".  

Part 1 is the local version - the client that's in your computer.  Think about it like how when you connect to the internet, you'll need a web browser.  So everything that you do in that client until a certain point (called `git pull`) is only local to your computer.  Why is this?  There are the reasons:  
- 1st: If you don't have internet access, you can still use version control in your local machine.  
- 2nd: If you are working on something that you don't necessarily think is good enough or not ready yet to upload and merge with the rest of the project, you can do it this way.  
- 3rd: It's so that if you are working on a project with others, or even working on your own existing project, you can create what's called a `branch` and mess around in it as much as you want.  If you accidentally mess up, you know that there's a known good version that's existing somewhere.  

![The power of branching compels you! (picture of 2 dogs running away with a branch)](/images/ThePowerOfBranchingCompelsYou!.gif?raw=true "The power of branching compels you! (picture of 2 dogs running away with a branch)")  
Branching is where the true power of `git` lies.  As far as I've seen, other version control systems don't have it.  With branching, a user can make branches with experimental work, and testing and checking it first, before re-integrating this work with the rest of the project.

Part 2 is the remote version.  The remote version is called a "repository", which is often shortened into "repo".  Either GitHub or GitLab can be used for these.  

(OPINION: For game dev, which deals with a lot of large files, I think it's better to use GitLab, just because you don't need to pay extra to use `git-lfs`.  Although, the cool thing about using GitHub is that currently, all active repos are backed up in Arctic World Archive in Svalbard, Norway (https://archiveprogram.github.com/).  But you would need to do some extra setup for the large files, and you would need to have another way to share and collaborate on those said large files.  GitHub also has a Unity plugin [https://unity.github.com/].)

I have a dream....  
Full disclosure, I do not work for `git`, or GitHub, or GitLab.  I am but a humble I.T. (with some art background)-turned videogame-programmer.  But if it were up to me, EVERYONE will learn version control, not just programmers.  The reason for this is simple.  It will be easier for everyone to back up their work, and go back to known-good versions of their work in case something got messed up.  Then they would just be mildly annoyed, instead of panicking.  It doesn't matter if people are accountants, lawyers, paralegals, marketing, community managers, artists, designers, animators, scientists, mathematicians, etc.  I really sincerely think that this will be a helpful tool for anyone, so I have a dream that everyone will make git version control a part of their workflow, and I hope that this guide will be useful for as many people as possible! ^-^

| [Back: Main Table Of Contents](/tutorials/TABLE_OF_CONTENTS.md) | [Next: First-Time-Setup Instructions](/tutorials/First-Time-Setup_Instructions.md) |
| :-: | :-: |
