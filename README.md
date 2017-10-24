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
    * 
3. Next, we will be creating an SSH key.
    * Click on your new profile picture icon (located on the top-right corner), and navigate to 'settings'
    * On the left, go to "SSH and GPG".
    * Next, make a new SSH key, and title it as "cloud9".
    * In order to access your new key:
        * Go to your [Cloud9](c9.io) account, and click the gear icon on the top-right.
        * Go to "SSH Keys", and copy the **second** key (starts with _ssh-rsa_). Go back into your Github account, go to settings and into "SSH and GPG keys". Press "New SSH key" and paste the second key.
        * Inside of your Github workspace (most likely named github-learning IDE), type in "ssh -T git@github.com"
            * You should then get a message saying "Hi <your username>! You've successfully authenticated, but GitHb does not provide shell access._"

* Now you are ready to start coding with your new GitHub workspace!

---
## Repository Setup



---
## Workflow & Commands



---
## Rolling Back Changes