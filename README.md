# GitHub Tutorial

_by Emily Saloma_

---
## Git vs. GitHub
Both Git and Github are version control systems (a system used to tracks changes made in repositories), and use similar commands to create and make changes to repositories. However, there are some differences between the two:
| Git  | Github |
| ------------- | ------------- |
|  Git uses 'snapshots' to record code, and does not need Github in order to function. | Unlike Git, Github can save any code in a cloud (you have access to it whenever you want), show what changes are made inside of the code, and can be shared with others to work on projects. Although Git does not need Github, Github requires Git.|

---
## Initial Setup

With Github, you can make all kinds of things- websites, apps, and so much more! And it doesn't take much to make an account for Github too. Just follow these steps:

1. [We start by going to the Github website.](www.github.com)
2. The website will guide you through a step-by-step process on how to make your account:
    * Fill in your information- a username, email, and password (which must have at least 7 characters). Once this is done, and account will automatically be made for you.
    * Next, you will be asked to choose a plan.
        * One of the plans give you unlimited _public_ repositories for free, while they other gives you unlimited _private_ repositories for $7/month. Personally, I would recommend the first plan for beginners, and upgrade later on if you feel confident enough.
    * Finally, you will be asked to fill out a survey based on your programming experiences. You can choose to complete the form, or just skip it entirely.
    
3. Next, we will be creating an SSH key.
    * Click on your new profile picture icon (located on the top-right corner), and navigate to 'settings'
    * On the left, go to "SSH and GPG".
    * Next, make a new SSH key, and title it as "cloud9".
    * In order to access your new key:
        * Go to your [Cloud9](c9.io) account, and click the gear icon on the top-right.
        * Go to "SSH Keys", and copy the **second** key (starts with _ssh-rsa_). Go back into your Github account, go to settings and into "SSH and GPG keys". Press "New SSH key" and paste the second key.
        * Inside of your Github workspace (most likely named github-learning IDE), type in `ssh -T git@github.com`.
            * You should then get a message saying "Hi <your username>! You've successfully authenticated, but GitHb does not provide shell access._"

Now you are ready to start coding with your new GitHub workspace!

---
## Repository Setup

Before we start making your first repository, let's get a general idea of what each code does.

* **`cd`** = to change directory or move through files.
* **`mkdir`** = makes new files.
* **`git init`** = to initialize (or start) a repository.
* **`touch (README.md)`** = makes a "document" or a place to store text inside a file (which is where this tutorial is being typed in).
* **`git add .`/`git commit -m "<text>"`/`git push`** = allows a person to save their progress in GitHub and leave a note at that point in the code.

Now, let's make our first repository!

1. Make sure your in "workspace" first (if you are unsure of where you are in the code, use cd ~/workspace)
2. Next, use `mkdir` to make a new repository (i.e. mkdir first-repo).
3. From the workspace, change directory (cd) into the first-repo (cd first-repo)
4. Finally, type in `git init` to initialize the repo.
    * **Make sure you are in the "first-repo" repository when using `git init`.**


Say you now want to make a file inside of this repository. This is how you would do it:

1. First, make sure the remote repository was made.
    * To make a remote repository, go to [GitHub](github.com) and press the "+" on the top right. Press "new repository" and name the repository "first-repo".
2. Inside of "first-repo", type in `touch README(or any name).md`. To open the file, you have to directly click on it on the left side-bar.
3. Type away whatever you want inside of the file. After you are done making changes to the file, make sure to save, add, commit a message (it is recommended to make the message relevent and useful for you), and push. 


Congrats! You have successfully made your first repository and file in Github!

---
## Workflow & Commands

Now that you've got the hang of using GitHub, let's review some more commands in-depth:

* **`git status`:** Git status is used to list all of the files and keep check on any progress made in a repository. Usually if you are coding for a big project and don't know where you are at, git status is a great way to get an understanding of what you're doing.
* **`git add .`:** Git add revamps any files in the repository to the index. This command is usually followed after with...
* **`git commit -m`:** Git commit helps us make note of what is going on in the code, similar to making a comment. This command is used after git add, and is accompanied by...
* **`git push`**: Git push upgrades the remote repository with any changes made in the repository since your last commit.

---
## Rolling Back Changes

Sometimes while using GitHub, you could being coding something amazing until...

Oops! You didn't mean to push that commit, or even mean to make a commit in the first place!

If you mess up a commit while editing code, that is okay! Sometimes we make mistakes, and it is from those mistakes where we learn from the wrong, and learn to make it right.

That being said, there are ways to go back to a previous step in case you messed up on some code:

* To undo an _edit_, use "`git checkout -- [insert file name]`"
* To undo an _added_ command, use "`git reset HEAD [insert file name]`"
* To undo a _commit_, use "`git reset --soft HEAD~`"
* To undo a _push,_ you can...
    * Use `git reset HEAD ~1` (to go back to the edit)
    * Use `git reset --hard HEAD~1` (to undo farther then an edit).

In extreme cases where you need to undo _pushed commits_, you can do these steps:
* `git revert`...
    * `a867b4af` (for the **most recent** commit)
    * `b5eee4ca` (for the **second most recent** commit)
    * `c766c053` (for the **third most recent** commit)
* **`git reset --hard 0d1d7fc32`**
* **`git push origin +master`**


**Note: Those listed in bold will reset past history and delete _ALL_ commits, so be careful before using them.**

---

## Error Handling

When using GitHub, there can be a multitude of things that can and will go wrong. Generally, most of these mistakes are small and can be resolved by using `git status` to check for any errors. However, there are some exceptions:

As mentioned above, **make sure to be in a repository when using `git init`**. If you do `git init` in the workspace, it will be initialized (which you can tell if you see workspace (master). If you do accidentally do this however, type in `rm -rf .git`, which will remove the local repository and return you back to your workspace.

* As a side note, if you want to remove a repository (remote, not local), first you would use `git remote rm [name of remote]` and follow it up with `git remote -v`.

---

## Collaboration

Your GitHub repositories are not only just limited to you, but you can also share and allow people to join as well! And there are many ways to interact with one's repos:

* **Cloning:** This method allows you to make your own copy of another person's repository, which allows you look at it but not interact with it's code.
* **Forking:** To "fork" someone's repository is similar to that of cloning, except now you can make edits to the repo. This allows you to make any changes you want to your copy of the repo, which you can then send to the original poster via "pull" requests".

Note: Both forking and cloning require for you to copy and paste the repo's url (SSH) into your workspace before being able to do anything mentioned above.

---

Now that you have the basics down: "git" more practice, "git" experience with collaboration and experimenting, and "git" better!