# Week 1

## Computer Setup

It is a lot of work to setup your computer for machine learning with Python. Please set aside at least an hour to go through the computer setup, and read the instructions carefully.

1. [Code Editor](#code-editor)
2. [Installing Git](#installing-git)
3. [Using GitHub](#using-github)
4. [Installing Python](#installing-python)


### Code Editor

While your professor may show you some [Jupyter notebooks](https://jupyter.org/), you will primarily write code in a code editor during this course. We recommend using [Visual Studio Code](https://code.visualstudio.com/), but you are free to use whatever code editor you prefer.

### Installing Git

If you have not already created an account, go to [GitHub](https://github.com/) and create one.

#### Mac Setup

1. Install [brew](https://brew.sh/), the homebrew package manager.
2. In Terminal, run `brew install git`.
3. If you type `which git` then you should see a path to the location where git was installed, such as `/opt/homebrew/bin/git`.
4. Set your Git username and email by running the following in your terminal (replace `your_username` with your GitHub account's username).
    ```commandline
    git config --global user.name “your_username"
    ```
    Check if this was done correctly by running the following, and you should see your user name print out:
    ```commandline
    git config --list | grep user.name
    ```
    Finally, run the following (replace `your@email.com` with the email you used for GitHub).
    ```commandline
    git config --global user.email “your@email.com”
    ```

#### Windows Setup

1. Go to [Git For Windows](https://gitforwindows.org/), click `Download`, and open the downloaded file to install Git.
    - On the "Select Components" screen, check "(New!) Add a Git Bash Profile to Windows Terminal".
    - On the "Default Editor" screen, select your editor of choice (e.g. Visual Studio Code).
    - On the "Adjusting the name of hte initial branch..." screen, select Override and set the value to `main`.
    - For the rest of the installation, use the defaults.
2. After installing, open Git Bash.
    - Protip: you can paste code into Git Bash by pressing `Ctrl + Shift + Insert`.
<!--TODO! See if this works -->
3. Set your Git username and email by running the following in your terminal (replace `your_username` with your GitHub account's username).
    ```commandline
    git config --global user.name “your_username”
    ```
    Check if this was done correctly by running the following, and you should see your user name print out:
    ```commandline
    git config --list | grep user.name
    ```
    Finally, run the following (replace `your@email.com` with the email you used for GitHub).
    ```commandline
    git config --global user.email “your@email.com”
    ```

### Using GitHub

#### Setting up SSH 

1. Go to [this page](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) and follow the instructions up until the section titled "Generating a new SSH key for a hardware security key". Note: you can adjust the instructions for you operating system (Mac vs. Windows).
2. Go [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) and follow the instructions to add your new SSH key to your GitHub account.
3. Test your connection by going to [this page](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection) and following the instructions.

#### Creating a Repo

1. Go to https://docs.github.com/en/get-started/quickstart/create-a-repo and follow the first 6 steps to create a repository.
    - A repository is like a folder that contains the files for a coding project.
2. Now, _clone_ (aka download) your new repository to your laptop. Go to the main page for your new repository and click on the Green `<> Code` button.
3. Click `SSH` and copy the text underneath that starts with `git@github.com:`.
4. From Terminal on Mac or Git Bash on Windows, run the following where you replace `$GIT_URI`` with the text that you copied in the previous step.
    ```commandline
    git clone $GIT_URI
    ```
5. The repo should now be on your laptop (type `ls` to see if it's in your current directory).


#### Modifying Code Online

Through GitHub, you can modify your code online.

1. Go to your hello-world repo, and click on README.md
2. On the upper right above the file's contents, click on the ✏️ (pencil symbol) to edit the file.
3. On the the `Edit file` tab, add some new text to the file.
4. Under `Commit changes` add a _commit message_ where it says Update README.md in grey letters.
    - A “commit” is a logical change to your codebase. This could consist of multiple changes to multiple files, adding a file, removing a file, etc… The idea is that this is a collection of changes that are related to each other.
    - Each commit gets a “commit message”. This is a small piece of text to explain what the commit does (e.g. “Allow users to login from Facebook”. “Remove old files”.)
5. Click the green `Commit changes` button to make your changes “official”.

#### Pulling and Pushing


##### Pulling 

You have now changed your code on GitHub. On your laptop, in Terminal/Git Bash, navigate to your `hello-world` directory that you cloned in the [Creating a Repo](#creating-a-repo) section and run 

```commandline
git pull
```

This will _pull_ the latest changes from GitHub to your laptop. You should see that your _local_ copy of README.md has been updated (you can open it in your text editor or run `cat README.md`).

##### Pushing

1. You can now go through a similar process where you change your code on your laptop and _push_ the changes to GitHub.
2. Open README.md in a text editor, modify it, and save it. 
    - If you've installed Visual Studio Code, you can open your current directory from the command line by running `code .` (note the `.` at the end).
    - If you're on Windows, you may have to run this command from Powershell.
3. We now must _commit_ the changes to README.md
4. In Terminal / Git Bash, run the following to tell `git` that you would like to include the current changes to README.md in your next commit.
    ```commandline
    git add README.md
    ```
5. Run the following to create a commit of all of your changes with a commit message
    ```commandline
    git commit -m "Some commit message"
    ```
6. You have now committed these changes to your laptop. Run the following to push your changes from your laptop to GitHub.
    ```commandline
    git push origin main
    ```

#### The Course Repo

All homework and notes will be distributed via this course's GitHub repo. You should keep a copy of this repo on your laptop. How do you do this? You should clone this repo to your laptop.

We will update this repo throughout the course. You can pull the latest changes to the repo onto your laptop by running `git pull` from within the main directory of this repo.

### Installing Python

There are many ways to install Python and manage third party Python libraries. If you feel very confident in your Python setup, then you may continue with your method of installing python and associated dependencies. Otherwise, in this course we will strongly recommend that you use [tye](https://rye-up.com/). Even if you already have a Python setup that you're comfortable with, installing `rye` will not affect it, so you should feel comfortable installing it. We recommend `rye` for a couple of reasons:

1. It works on Mac, Windows, and Linux.
2. It installs Python for you.
3. It manages the _version_ of Python that you install.
4. It resolves third party dependency conflicts.
5. It encourages best practices of structuring your code as a Python _package_ rather than as a collection of scripts.

`rye` is somewhat similar to [Anaconda](https://www.anaconda.com/), which some of you may be familiar with. While Anaconda does handle the first 3 steps above, it does not handle Python packaging. Additionally, we have found that Anaconda is often not used within companies due to difficulties in publishing and installing private, internal packages.

### Setting up Rye

##### Windows Instructions

1. Turn on Windows Developer Mode ([see instructions](https://rye-up.com/guide/faq/#windows-developer-mode)).
2. Go [here](https://rye-up.com/guide/installation/), click the `Windows` tab, and download the `.exe` file.
3. Open the file. Windows will tell you not to do this. Click `More Info` and then click `Run Anyway`.
4. Follow the instructions to [Add Shims to Path](https://rye-up.com/guide/installation/#add-shims-to-path).

##### Mac Instructions
1. Go [here](https://rye-up.com/guide/installation/), click the `Mac` tab, and run the command that starts with `curl`.
2. Go down to the [Add Shims to Path](https://rye-up.com/guide/installation/#add-shims-to-path) section. If you know what type of shell you have, then follow the instructions for your shell. Otherwise, click `ZSH` and run that command.

##### Test Driving Rye

Instructions for making your own project:

1. Open `PowerShell` or `Git Bash` on Windows or `Terminal` on Mac and run `rye init my-project`. This will create a new directory and python project called `my-project`.
6. Move into the current directory by running `cd my-project`. 
7. Run `rye pin 3.11` to ensure that you only use Python version 3.11 in this project.
8. Run `rye sync` to download Python.
9. Add the [cowsay](https://pypi.org/project/cowsay/) dependency by running `rye add cowsay`.
10. Run `rye sync` to install `cowsay`.
11. Test that everything worked by running 
    ```commandline
    python -c "import cowsay; cowsay.cow('good job')"
    ```
    You'll know that everything worked if a cow says you did a good job.
12. Read more about `rye` by starting at the [rye basics guide](https://rye-up.com/guide/basics/).

