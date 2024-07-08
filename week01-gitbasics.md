# Week One - Git Basics
## What is Git
Let's take about what Git is and what makes it different.
- **Track changes over time**
	- Git is a tool to help you track changes over time. 
- **Backup & restore**
	- It lets you backup and restore files from different key points in a project's history. 
- **Distributed version control**
	- It's known as Distributed version control because it's designed to be used by multiple users. 
- **Designed for multiple editors**
	- Each user can have a complete copy of the entire project locally, allowing them to work even offline. Git provides tools for managing changes users create on similar files.

---
## Multiverse Time Machine
In essence, Git is a multiverse time machine, somewhat similar to what you see in Marvel or Star Trek movies. It lets you travel back in time to difference checkpoints you save and lets you create alternative timelines to try out new code.

- **Repo** (repository)
	- The place where the data is stored is called a repository or repo for short. This data is stored in an invisible folder that keeps the history of the changes made to the files. Git only keeps track of original files and any changes that have been made to them. Repositories can be stored locally or remotely.
- **Check points** (commits)
	- With Git, you can lock in time codes that you may want to go back to go back to later on. These are known as commits. Each commit will have an ID, and lock in the current status of all of the files in the tracked folder.
- **Alternate history** (branches)
	- You can create an alternate history of the project by creating different branches. That creates a new universe where you or others can experiment without messing up the main version of the project. You can create as many branches as you like.
- **Synchronization** (merging)
	- When you're ready to lock in the changes on the official (main) version of the project, you perform a merge command. That allows you to synchronize the different versions and bring the main branch up to date.
- **Publishing** (pull/push)
	- Projects are usually published on a remote server, know as the origin, which allows many people to have access to the project. As an individual you can pull to get information from the server, or push to send your changes.

---
## Set up commands
Once you've downloaded and installed Git, there's a few basic set up commands you should be familiar with.

- `git init`
	- The `git init` command creates an invisible `.git` folder, which git uses to store the changes to the files being tracked by the application.
- `git status`
	- The `git status` command lets you know the status of your files. 
	- Git will give you a detailed description of what's happening with your documents. 
	- It will also give you some instructions as to what you need to do to change things.
- `rm -r .git`
	- You can ask git not to track your files any longer by removing the `.git` folder using `rm -r .git`. This can be dangerous because it removes all history, but it can also be beneficial when you are starting a new project based on an old one or want to start your history fresh.

---
## Working Directory
The working directory is the folder where you `.git` folder lives and contain the files git is tracking. Files in the working directory can be in different states.
- **Untracked**
	- You can have files in your git folder that are not yet part of the repository, these are known as untracked files. 
		- These files are not included or stored in the history. 
		- This can happen when you first create a repo
		- It will also happen when you copy or create new documents inside the repo folder.
- **Modified**
	- If a file has previously been committed and is then changed, then it's going to be in a modified state. 
	- It can be reverted back to its original state or staged for later committing.
- **Staged**
	- Modified files can be moved into a temporary queue called staging. 
	- This will let you store changed files to keep track of what will be committed. 
	- Files can move from staging back to working. To stage files, you can use the `add` command.
- **Committed**
	- This is the process of saving changes in staging to history, locking in a place that you can always come back to. 
	- It stores  the name and email of the person who made the commit, the date when the commit was made, a user message and an ID for the commit. 
	- After the changed files will be in a working state.

---
## Staging Files
Let's talk about the process of moving files into the staging state. There's a few [commands](https://git-scm.com/docs/git-add) you can use. 

- `git add <filename>`
	- This allows you to move one or more files to staging. 
	- You can stage individual files by using git add and then specifying a filename you want to add.
	- That filename can support any file glob or shortcut.
- `git add .` `git add *` `git add --all` `git add -A`
	- If you want to move all modified or untracked files to staging, these commands will add all of the modified files into staging. 
	- This is probably one of the most common way to add files. 
	- You can of course use any file shortcut like `*.js` to add all of the javascript files in the current directory.
- `git rm --cached <filename>` `git restore -S <filename>`
	- These command let you move files out of staging and back into untracked. 
	- If you add the `-r` option, it will recursively let you remove a bunch of files at once. 
	- It's a bit hard to remember, but you can always let the `git status` command remind you.
### Exercise
Let's practice moving files in and out of staging.
- Stage a single file
- Unstage a file
- Stage all files
- Unstage all of the images using `git rm -r --cached images/**`
- Let's stage all the images using `git add .`

---
## Committing files
To create a commit, you can issue a [commit command](https://git-scm.com/docs/git-commit). this saves staging to history, locking in a place that you can come back to. After the changes files will be in a working state.
* `git commit -m "Message"`
	- You can commit files using the `git commit` command, it requires that you give it a message recording what you're doing.
	- The message acts as a label you'll see when going over a list of commits.
	- It can be quite complex and include the changes you've made to the files since the last commit, but the most important part is the label, since it's what you'll see most often.
	- The shortcut for the --message option is -m
- `git commit -m --dry-run "Message"`
	- The `--dry-run` option lets you take a look at the changes you're making, so it might be helpful when writing your message.
- `git add . && git commit -m "Message"`
	- Some people will use the double ampersands to queue up two git commands together, specially the add and commit commands.
- `git log`
	- Lets you look at the history of commits: It stores  the name and email of the person who made the commit, the date when the commit was made, a user message and an ID for the commit.
### Exercise
Let's try committing all of the files from staging.
`git commit -m "Initial Commit"`
- The -m is required and lets you add a message to your commits
- It's a shortcut for --message.
- Let's issue a git status command to see what's going on.
`git status`
Now we have a clean working tree.
`git log`, then `q`
Lets take a look at the information that Git is saving about our project. You can scroll down to see a longer list and hit the `q` key to continue.

---
## Ammending Commits
An amend will add modified information or changed files to an existing commit.

- `git commit -m --amend "Message"`
	- You use it if you forget to commit something or want to make some minor modifications to a commit.
	- This is also a way to change the commit message, if you made a typo or want to add some context
	- **Warning!** This does not add untracked files to your commit, so if you have created or copied new files, you'll need to add them first.
	- **Warning!** This is good for local commits, or when working solo, but can be dangerous when working in a team environment, if someone has work based on the previous version of a commit.
-  `git commit -am "Message"`
	- You can use `-a` as the shortcut for the amend command.
- `git commit -am --no-edit`
	- The `--no-edit` option leaves the old commit message unchanged.
### Exercise
Let's try adding a `README.md` file to our project, I [created one](https://gist.githubusercontent.com/planetoftheweb/aa7731b1d782082f71b38cc89ff4d9de/raw/038609b40822b6388d176d22a2c0c06a219f4f7d/README.md) for you.
- Don't copy all of the text, start by copying only the **Title and Description** in the [README.md](https://gist.githubusercontent.com/planetoftheweb/aa7731b1d782082f71b38cc89ff4d9de/raw/038609b40822b6388d176d22a2c0c06a219f4f7d/README.md) gist.
- `git add .` and `git commit -m "Message"` the file with a simple message
- Issue a `git log` command to see information about your commit.
#### Practice a no-edit option
Using a no-edit option to add to an existing commit
- Copy the [next section](https://gist.githubusercontent.com/planetoftheweb/aa7731b1d782082f71b38cc89ff4d9de/raw/038609b40822b6388d176d22a2c0c06a219f4f7d/README.md) of text to the file titled **Techniques Used** and Paste them into the `README.md` file.
- Save it and do a `git status` to see that the file is currently listed as modified.
- Add the file using `git add README.md`
- Issue the `git commit --amend --no-edit` command to add the changes.
- **Note:** Remember that this works well for solo developers, but when working with a team pushing amends could cause problems for those who already pulled a previously committed history.
#### Untracked files
Untracked files will sometimes cause unexpected behaviors when committing and amending.
- Copy the [next section](https://gist.githubusercontent.com/planetoftheweb/aa7731b1d782082f71b38cc89ff4d9de/raw/038609b40822b6388d176d22a2c0c06a219f4f7d/README.md) of text to the file titled **Notable Libraries and Technologies** and Paste them into the `README.md` file.
- Add the file using `git add .`
- Now, create a new document on the same folder called `LICENSE.txt`. Add this [MIT license](https://gist.githubusercontent.com/planetoftheweb/7e254040a0525971c45295ddabf25e84/raw/b45be12298e44c52b241cdd759c703b404b48220/LICENSE.txt) to the document, then update it with the year and your name.
- Now you should have one untracked file and one modified file. Let's see what happens if you commit.
- Try a `git commit -m "Modified README and added a LICENSE"`.
- Issue a `git status` command. Notice that because the `LICENSE.txt` file was untracked, it wasn't committed and you didn't get any sort of error message.
- Now, let's use `git add .` LICENSE file and `git commit --amend --no-edit` to add the license and add it to our last commit.
- Issue a `git status` and `git log` command to verify the changes were logged in properly.
##### Note
I created this [README](https://gist.githubusercontent.com/planetoftheweb/aa7731b1d782082f71b38cc89ff4d9de/raw/038609b40822b6388d176d22a2c0c06a219f4f7d/README.md) using [Chat GPT](https://chatgpt.com/) and [this prompt](https://gist.githubusercontent.com/planetoftheweb/ddbf48aa93b6eac6508aaf690f03f236/raw/39489319b1ca054986e65600d3d525f8364c1da5/README%2520prompt%2520generator). AI is a great way to generate things like README files and other documentation about your project.

---
## Restoring Files
This command lets you revert changes in the working directory and staging area. It makes it easy to revert files to a previous version.

- `git restore <filename>`
	- This command discards changes in the working directory. It's a newer command with a single purpose.
- `git checkout <filename>`
	- This does the same as git restore and is a popular older version of the command. Checkout allows you to do other things as well.
- `git restore --staged <filename>`
	- The `--staged` option will also **unstage** the files.
- `git restore --source <commit> <filename>`
	- You can also restore a file to a different commit, so if you want to bring a file back from a previous version you can do that by including a commit hash id.
### Exercise
Let's try the restore command a few different ways.
#### Restore to last commit
- Copy the [next section](https://gist.githubusercontent.com/planetoftheweb/aa7731b1d782082f71b38cc89ff4d9de/raw/038609b40822b6388d176d22a2c0c06a219f4f7d/README.md) of the `README` file titled `Notable Libraries and Technologies` and paste it into the `README.md` document.
- Make sure you save the file.
- Use the `git status` command and notice that it lists a modified file not staged for commit.
- Use the `git restore README.md` command.
- Git restores the previous version of the file.
#### Using the --staged option
`git restore` doesn't work on staged files, so to restore that you have to use the `--staged` option.
- Paste the section of the file again (or use undo) to update the `README.me` file.
- Issue a `git add . command` to stage the file
- Try issuing a `git restore` command. Notice the file still has the new changes.
- Run `git status` and notice that the file is still in staging ready to be committed because restore by itself won't have an effect without the `--staged` option.
- Run the `git restore --staged .` command, and you can see that the period command will restore all the staged files, but leave the changes.
- If you want to get rid of the changes, issue the `git restore .` command.
- Go ahead and add the changes, then commit them as a new commit called "Added Notable Libraries and Technologies"
#### Restoring a different commit
You can also restore a previous version from an older commit.
- Select everything in your `README.md` file and `delete` the content, then `save` the file.
- Issue a `git log --oneline` and copy the **hash ID** for a previous commit.
- git `restore --source <hash_id> README.md`
- Try restoring to a different ID.
- When you're done, use `git checkout .` to get the  version of the file from the last commit.

---
## Rewriting History
When you make a mistake, you can use the [git reset](https://git-scm.com/docs/git-reset) command to reset history to a previous commit ID. This rewrites the position of the HEAD pointer, whereas restore leaves it alone.

- **HEAD pointer**
	- When you use the git log command, you'll noice that there's something called a HEAD pointer at the top of your commit messages. This represents the tip of your current branch.
- `git reset HEAD~1`
	- The default mode for resetting is called mixed mode, so this is the same as adding a `--mixed` option.
	- The `HEAD~1` part tells git to go back one commit. You can of course go back more than one commit. If you want to go back to a specific commit, you can also include a hash of the commit instead of `HEAD~1`.
	- This will reset your commit to the previous version.
	- It also un-stages the files, but it doesn't get rid of any changes you made, it leaves the files changed as modified.
- `git reset --soft HEAD~1`
	- The **--soft** option does the same thing, but it leaves files in staging instead of as modified or untracked.
- `git reset --hard HEAD~1`
	- The `--hard` option gets rid of all changes in staging and the working directory.
### Exercise
Let's practice using these different options.
#### Mixed Reset
- Modify the `README.md` file to include a new headline `## Bogus Info` 
- Make sure you save the file.
- Issue a `git add .` and `git commit "bogus commit"`
- Issue a `git log --oneline` command to verify the new commit is in history and hit `q` to exit the log.
- Now, let's use a `git reset HEAD~1` command.
- Notice the file keeps the `Bogus Info` headline
- Issue a `git status` command to verify the README.md file is not staged for commit.
#### Soft Reset
- Issue a `git add .` and `git commit "bogus commit"`
- Issue a `git --oneline` command to verify the new commit and hit `q` to exit the log.
- Issue a `git reset --soft HEAD~1` to reset the file.
- Issue a `git status` command and note that `README.md` file is in the staging area ready to be committed.
#### Hard Reset to a Specific Commit
- Let's add some extra text under the `Bogus Info` headline with the text `Additional bogus information` 
- Make sure you save the file.
- Issue a `git add . && git commit -m "Additional bogus commit"` command.
- Issue a `git log --oneline` to make sure the new commit exists.
- Copy the short hash id (i.e. d697c6f) to the commit you want to revert to, then hit the `q` key to exit.
- Issue a `git reset --hard ID` where the ID is the number you copied.
- Notice all your changes have been removed.
- Issue a `git log --online` to verify the bogus commits are gone.

---
## Ignoring Files
When working with projects, sometimes you want to prevent certain files or patterns of files to be ignored. To do that you can create a special dot file
- **Root Level**
	- The `.gitignore` file should be added to the root of your project.
- **Files, Folders and Globs**
	- It can list individual files, folders or file patterns that you want git and GitHub to ignore, so these will not be pushed onto GitHub.
- `.DS_Store`, `Authentication.js`, `dist`, `build`, `node_modules/`, `logs/*.log`, `.env`, `**/*_note.md`
	- Here's some common `.gititnore` files
	- `.DS_Store` is a hidden mac file that is not relevant to your project, but might be added by the OS. 
	- `Authentication.js` or similar files are documents that you might need in order to work with external APIs. They're named different things, so adjust as needed.
	- , `dist/`, `build/` are folders that different tools will create for you and sometimes you don't want the generated folders to copy to a server.
	- `node_modules/` is a folder with dependencies that are common for web projects.
	- Some projects create log files, so `logs/*.log` is also a good thing to add here.
	- `.env` environment files provide a way for you to 
	- You can create your own set of files that will not upload. `**/*_note.md` 
### Exercise
Create a new `.gitignore` file at the root level of your project.
- Add any files or globs that you think your project might use.
- Add a `**/*_note.md` glob to exclude any files with the `_note.md` extension.
- Use the `git add .` and `git commit -m "Added a .gitignore file"` commands to add and commit the file.
- Create a `main_note.md` file
- Use the `git status` command and note that it says there's nothing to commit.
- Create folder called `notes` and add a `local_note.md` file inside it.
- Use the `git status` command and it should also say that there's nothing to commit.
#### Note
Empty folders are not tracked or uploaded to GitHub. If you want to makes sure a folder gets uploaded to GitHub, you can just add a `.gitignore` or any other dot file like `.gitkeep`, even if they're empty.

---
## Creating Branches
So far, we've been working by making changes to the main branch. The traditional way to work with project is to leave the main branch alone and do your work in a separate branch. This is known as Gitflow.
- `git branch` 
	- Shows you the current branches in the project, the default branch is traditionally called `main` or `master`.
	- A branch copies all of the previous commit history from the branch it is issued from.
- `git branch <name>`
	- This creates a new branch with a name. Traditionally the name refers to a feature we want to work on and is sometimes called a feature branch.
- `git checkout <name>` `git switch <name>`
	- These commands allow you to go to a specific branch.
- `git switch -c <name>` `git checkout -b <name>`
	- You can also create branches and switch to them immediately with these options. 
	- Switch is considered a newer, clearer version of the command and the -c version stands for create.
	- A lot of people use checkout and if you add the -b for branch option, you can create and switch just like with switch.
- `git branch -D <name>` 
	- You can delete a branch with the -d option
	- It's common to delete a branch once you're finished with a feature and it has been merged back into the main branch.
- `git branch -m <original_name> <new_name>`
	- If you want to rename a branch, you can use the move option and add the original name and the new name.
### Exercise
Let's practice creating and navigating through branches.
#### Creating Branches
- Issue the `git branch` command to take a look at the current available branches, there should only be a single branch.
- Create a new branch using `git branch add_fonts`
- Switch to the new branch using `git switch add_fonts`
- Issue a `git log --oneline` command and notice that all of the commit history has been copied from the main branch.
#### Modifying Branches
- Add the section titled `Fonts` to the `README.md` document.
- Issue `git add .` and `git commit -m "Added Fonts Section"` commands to create a new commit.
- Issue a `git log --oneline` command to see the log and notice the place where a new branch was created and the position of the HEAD pointer. Hit `q` to exit the log.
- Issue a `git checkout main` command to go back to the main branch. Notice the changes are gone.
- Issue a `git log --oneline` command to see that the log doesn't have the changes.
#### Deleting branches
- Switch back to the previous branch with `git switch add_fonts`
- Create and switch to a new branch using `git switch -c new_branch` 
- Issue a `git log --oneline` and notice that it copied the last commit. Hit `q` to exit the log.
- Issue a `git switch main` command to switch back tot he main branch.
- Use `git branch -D new_branch` to delete the new_branch

---
## Merging Branches
Merging allows you to integrate changes from one branch to another. It's often used to move things from feature branches onto the main branch.
- `git merge <source-branch>`
	- The merge is always done into the current branch, so this command would add changes from the from the `source-branch` into the current branch
	- This is know as a `fast forward` merge and is the simplest type of merge you can do.
- `git log --graph` is a version of git log that shows the flow of the merges.
- Merges can be of different types and require different approaches when you need to resolve them.
### Exercises
Let's practice some merging of our projects. I'm assuming you still have a branch called add_fonts with the fonts section of the README file.
#### Straightforward Merge
Lets create a straightforward merge
- Issue a `git branch` command to get a list of branches and verify that you still have the `add_fonts` branch.
- If you're not in the main branch, issue a `git switch main` command to make sure you're on the main branch.
- Issue a git merge `add_fonts` command to add the changes in `add_fonts` to your `main` branch.
- Use a `git log --graph` to see the flow of the commit.
#### Merge with a conflict
Sometimes, you can try to merge a branch, but you've already made changes to the branch you want to merge into, so a different approach is necessary.

- Assuming you're in the `main` branch and that you still have a branch called `add_fonts`.
- Issue a `git log --oneline` and look for the commit hash ID that's before the commit where you added the fonts.
- Issue a `git reset --hard <hash_id>` to reset back to that commit.
- Now, let's say that you wan to change the title of the section from `Project Structure` to `Repo Structure`. Go ahead and make that edit and save the file.
- Issue a `git add . && git commit -m "Modified Title"` command.
- Now, let's try to merge the work we did in add fonts and remember that our main branch is currently ahead of that branch, so issue a `git merge add_fonts`
- You will get the option of adding a merge message. You can edit it if you like, but to get rid of it, you can simply close the window or the file in your default editor.
- **Notice** that git merged the two files and the two commits and it did so using an 'ort' strategy.
- Issue a `git log --graph` to visually see the two commits being merged into main.
- **Warning!** Sometimes, git will ask you to verify or write a commit message in an editor. The default editor will depend on your operating system. 
	- After you install Visual Studio Code, make sure you use the command palete and look for the
	- - Select **Shell Command: Install 'Code' command in path** from the Command Palette.
	- **Mac:** `shift + ⌘ + P` while inside VS Code **Windows:** `shift + ctrl + P`, make sure you select **Add to PATH** during the installation.
	- You can set up the default editor to be Visual Studio code using this command: `git config --global core.editor "code --wait"`
#### Merging Two Branches with Changes
You can also resolve changes in different branches
- Issue a `git log --oneline` to get a list of the hash IDs for your commits. Copy the hash ID for the commit before you added the fonts section. Hit `q` to return.
- Issue a `git reset --hard <hash ID>` command to revert to that commit.
- Use the `git checkout -b key_features` to create a new branch.
- Copy and paste the `Key Feature` section [from the file](https://gist.githubusercontent.com/planetoftheweb/aa7731b1d782082f71b38cc89ff4d9de/raw/038609b40822b6388d176d22a2c0c06a219f4f7d/README.md).
- Use the `git add . && git commit -m "Key Features" ` to create a commit.
- Use `git switch main` to go to the main branch
- Use `git merge key_features` to merge the newer branch.
- Use `git merge add_fonts` to merge the add_fonts branch.
- Now you have a **merge conflict**, which you need to resolve. Visual Studio code gives you some shortcuts you can use to accept the current change, the incoming change, or both changes.
- Because we want both changes, but they're not in the right order, we'll need to edit the file to make sure it's in the right order.
- Edit the file so it has the `Fonts` section, then the `Key Features` section.
- Use `git add .` and `git commit -m "Added Fonts and Key Features"` to add both changes.
- Use the `git log --graph` to see the commit graph history. Hit `q` to exit.
---
## Stashing Code
Stashing code can help you temporarily put away code that you can come back to.

- `git stash`
	- The main command to stash away changes temporarily is `git stash`
- `git stash list`
	- The stash is like a deck of cards, you can do multiple stashes and they'll go into a list of items. The last stash you did is at Stash 0 and the 
- `git stash pop` 
	- Git stash pop gets the last items stashed (item 0) and adds it back to the working folder.
- `git stash apply <ID>`
	- You can apply specific hashes by using git stash apply and then the ID you want to grab.
- `git stash clear`
	- This command clears out the stash.
### Exercise
A common reason to stash is when you start doing work in the wrong branch, like the main branch and realize you really needed to put it in a feature branch.

- Issue a `git switch main` to go to the main branch.
- Copy and paste the `External Libraries` section [from the file](https://gist.githubusercontent.com/planetoftheweb/aa7731b1d782082f71b38cc89ff4d9de/raw/038609b40822b6388d176d22a2c0c06a219f4f7d/README.md) into the `README.md` file.
- Save the document.
- Issue a `git stash` command
- Create a new branch using `git switch -c external_libraries`
- Use the `git stash pop` command to get the changes from your stash.
-  Issue a `git add . && git commit -m "External Libraries"` to commit the changes.
- Switch back to the main brach using `git switch main`
- Merge the branch using `git merge external_libraries`

---
## Creating A Repo
To push a repo to GitHub, we'll need to create it on GitHub first and then connect our local repo with the remote repository.

- [github.new](https://github.new)
	- This website lets you quickly create a new repo on GitHub. You have to have an account and also be logged in.
- **owner/name**
	- You'll need to choose an owner as well as a repo name, choose your username and github-demo for the name.
- **description**
	- A description will help people find your repo since it will appear on search results.
- **public/private**
	- You can choose between a public and private project. Remember that some features are only available for free on public projects.
- **README**
	- You can have the setup create a README file for you, this will have just a title, but it's a great way to get going quickly.
- **.gitignore**
	- You can choose a `.gitignore` file from a list of common versions. I've never liked the ones available so I usually ignore this and build my own.
- **license**
	- You can choose a license from a list of common licenses.
### Exercise
If you have an existing repo that you want to use, it's best to not add any default files, so let's see what it's like to link a local repo to GitHub.
- Go to `github.new`
- Choose `your account` as the owner
- Give the repo a name, you can use `github-demo`
- Make sure `Public` is selected to create a public repository.
- Don't use any other option and click `Create repository`
- Congratulations, you've created an empty repo. Look through the instructions to look at some of the options.

---
## Connecting to Remote
You can connect a local repo to a remote location like Github using the remote commands.
- `git remote add <remote-name> https://github.com/<username>/<reponame>.git`
	- The remote command is how we manage our connections to other places. 
	- The traditional `remote-name` is `origin` and it will be the default if you clone a repo from GitHub.
	- After the `remote-name` is the URL to Github, this usually have your `username` and `repository` name, but it can also have an `organization` name. It should also always end with `.git`
	- You can add multiple remotes if you want to 
- `git push -u <remote-name> main`
	- In addition to connecting to the remote, you also have to connect branches with their counterparts on GitHub.
	- The `-u` sets the default upstream branch for a branch, making pull and git push operations so you don't have to specify the remote and branch each time.
### Exercises
Lets connect our local repository to our GitHub repo.
- **Copy** the URL to your GitHub repository
- On your local copy of the repo, type in `https://github.com/<username>/<reponame>.git` using your username and reponame.
- Issue a `git push -u origin main` to push your main directory
- Go back to your GitHub Repo and see the updated repo.
---
## Using GitHub Codespaces
GitHub has a built in code editor you can use. It is a clone of Visual Studio code, but it has advantages over a local version.
- Go your Repository page
- Under the code button, switch to the CodeSpaces tab
- Hit the `Create codespace on main` button
- Wait until the codespace is launched
- `git push` will send changes from codespaces to the repo
### Exercise
Let's take advantage of GitHub Codespaces to make a change to your repo. 
#### Push Changes to Repo
- Update the title that says Fonts to Google Fonts.
- Make sure your terminal is open
- Issue a `git add .` and `git commit -m "Changed the Fonts Title"`
- Run a `git log --oneline` and notice that your new commit is done.
- Switch back to your repo and refresh. You'll notice that the change you made is not there.
- Issue a `git push` command to send your changes to the repo.
- Look at the commits section of the repo to look at your commits.
#### Updating your local commit
Now that we made changes on GitHub, let's pull these changes to our local repo.
- Open up the project in your local code editor.
- In the terminal Issue a `git pull` command
- Notice the `README.md` file updates.
- Do a `git log --oneline`
- Notice the new commit.
#### Rewind a commit
- Issue a `git log --oneline` and copy the hash to the commit before you added the fonts
- Run `git reset --hard <hash ID>`
- Try running a `git push` command again. Note that your push will be rejected because the repo has one more commit than your current repo.
- Issue a `git push --force` command to force push the changes.
- Go back to the repo and look at your commits, you'll see the commit messages are up to date.

