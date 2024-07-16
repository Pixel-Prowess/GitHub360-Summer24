# Week 02

## Repository Page

### Left Sidebar
The area at the top left of the site will have the name of the organization and/or repo with a dropdown menu that lets you get through the repo tabs, links to the [explore](https://github.com/explore) section and [marketplace](https://github.com/marketplace)and shows you links to your latest repositories, teams and common links.
### Toolbar
On the top right hand side, we get a toolbar with a number of icons that you can use 
#### Search
(hit the / to get there). By the way, you can also hit the ? to see keyboard shortcuts.
#### Add
This icon lets you add items like a [new repository](https://github.com/new), [import a repo](https://github.com/new/import), [create a codespace](https://github.com/codespaces/new), [a gist](https://github.com/gist), [an organization](https://github.com/account/organizations/new).

If you have an organization, there are some additional shortcuts here: invite people to your org, create a new team and add a repo to an org.
#### Issues
A quick link to all of your accounts issues in one button. More on these later.
#### Pull Request
A link to all your pull requests. More on these later.
#### Notifications
Look at the notifications for any of your projects.
#### Account Menu
A link to your account options, where you can get to your profile, 
### Repo Tabs
A tabs giving you access to the main features in repositories.
#### Code
This is the main tab for the repository with the code for the site.
#### Issues
Issues are the main and oldest way to discuss and create notes for repositories.
#### Pull Requests
When you modify code, you usually create a branch called a feature branch and then issue a pull request that tells someone managing the site that you'd like to issue a Pull Request, which proposes a change to the project. 
#### Actions
Actions are how you create automations for your projects.
#### Projects
Projects are how you manage the work you or your team does in a repo. Although it's listed here under a repository tab, in reality, its an account wide feature that has to be linked to individual repositories.
#### Wiki
Your sites can have Wikis associated with them. They are a very quick way to create documentation for a site.
#### Security
This is where you can set up security policies and other features for your site.
#### Insights
You can take a look at analytics of how your site has been used over time.
#### Settings
This is where you can control your individual repo's options. There are a ton of options and you can turn certain features on and off. We'll be talking more about these over time.

Notice that in the main section of the settings we can turn off features we're not using like Wikis and they'll disappear from the tabs, or we can add features like discussions and they'll take up a place in the tabs.

This is also where you can change a repo from public to private and delete a repository.

Another item of interest is the collaborators section where you can collaborate with others on your project.
### Social Menu
A few options here that let you control some of the social features.
#### Pin
You can pin your repos so they appear on your profile, but you only have six pin slots.
#### Notifications
Controls the notifications you'll receive about this repository.
#### Fork
Forking allows you to make a copy of a repository that is linked to the original. You can fork a repository, make a change and then issue a pull request to ask that your modifications be added to the original project.
#### Star
You can star a repo to give it props and create lists to keep track of your starred repos.
### File options
#### Branch/Tag Dropdown
You can take a look at your branches, create new ones and do the same for tags, which is what allows you to create releases.
#### Search in repo
You can find an item in the repository by using this search and open it up using the t key.
#### Add Files
You can create new files with this menu and upload files in this menu. You can also drag and drop files directly here.
#### Code
The code menu lets you control how people access the code in this repository. There are three options.
##### Local
Lets you control how you can get a copy of the repo for local use, you can use this to connect with the [GitHub Desktop](https://github.com/apps/desktop) application or local visual studio code.
##### Codespaces
Let's you manage and activate codespaces for the current repository.
##### Copilot
If you've paid for the copilot feature, you'll see it here as well. It can help suggest code changes to your repository.
### Right Sidebar
On the right, you'll see a repo details sidebar. You can see the details, website link and optionally releases, packages and deployments.
#### Releases
Releases point to official versions of your project that you can go back to. You create a release when you want to have a version of your projects that people can download. So you can create a version 1.0 and a version 2.0 release and that way people can still get to an earlier version of your application.
#### Packages
Packages are a special release that allows apps to use your projects as libraries or modules that can be loaded into other projects.
#### Deployments
GitHub can host your websites and deployments point to the different deployments that results as a part of that publishing.
## GitFlow
GitFlow is the process of updating things safely with Git. We've been practicing it locally, but you can do the same thing on Github. You create a branch, make changes on the branch and merge the changes to that branch onto the main branch.
### Pull Requests
On GitHub normally you perform one additional task in this process and that is called a Pull Request. Pull requests are formal requests for changes to be added to a website.
### Using the Website
You can use the website to add, delete and edit files directly without having to jump into a Codespace. Remember you can easily drag and drop documents and add folders or files.
### Exercise
To practice GitFlow, we'll use the website to add a default [settings.json](https://gist.githubusercontent.com/planetoftheweb/b840d7dad358cf1b79e543bfe3d8a036/raw/6b295971394e1c79fe58d5686fb8a6d2a044e22e/settings.json) file. This file will set up some defaults for Visual Studio code on this repository. The settings will automatically be used when you run a CodeSpace.
#### Adding a file
1. Go to the link for the [settings.json](https://gist.githubusercontent.com/planetoftheweb/b840d7dad358cf1b79e543bfe3d8a036/raw/6b295971394e1c79fe58d5686fb8a6d2a044e22e/settings.json) file.
2. Copy the text
3. Go to the repo for your site
4. The settings.json file needs to be inside a folder called `.vscode/`. To create a folder click on the `Add file` button.
5. Click on `Create new file`
6. Paste the contents of `settings.json`
7. At the top of the code, look for where you name your file.
8. Type in `.vscode` and hit the `/` key, it will create a new directory.
9. Name your file `settings.json`
10. Hit the `Commit changes...` button
11. You can leave the commit message and description alone if you want
12. Choose `Create a new branch for this commit and start a pull request`
13. Type in a name for the branch `add-settings`
14. Hit `Propose changes`
#### Using the pull request
That creates your branch and initiates a pull request. A pull request gives you an opportunity to discuss changes that are being proposed to the code before they get merged back to another branch.
This gives also gives you an opportunity to add reviewers, assignees, labels, projects, etc.
1. You can leave the title and description alone for now. 
2. Under Assignees, choose `assign yourself`
3. Under labels pick `enhancement` from the list.
4. Click on `Create pull request`

This will generate the pull request. Notice it also logged what you did, the adding of the file, the tag and your assignments.

Take a look around and notice the `commits`, `checks` and the `files changed` tabs.
#### Merge the pull request
You or other collaborators can add a comment to the pull request if you want to or simply merge the pull request to merge things into main.
1. Hit the `Merge pull request` button
2. Hit the `Confirm merge` button
3. Hit the `delete branch` button

The pull request will me merged into main and closed. Click on the `pull requests` tab and notice it says `0 Open` and `1 Closed`. You can still go back to the closed pull request if you want to know what it's all about.
#### Using the temporary editor
1. Go back in o the `code` tab.
2. Notice the `.vscode` folder is now there.
3. Hit the period key `.` on your keyboard.
4. This launches a quick version of the editor that is like a Codespace, but without the ability to run build processes on the terminal.
5. Examine the `settings.json` file in this editor.
6. Try changing some of the settings
7. Close the window to ignore the changes.
## Using Markdown
Markdown is a text based format that is easy to read and write and works well with GitHub. GitHub has it's own version called [GitHub Flavored Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github). You should become familiar with markdown features and how to write and link files using the format.

GitHub has an excellent built-in editor if you still want to use it to create documents without learning markdown.
## Issues
Issues are a way to create a document that people can discuss and contribute to. They are similar to pull requests but a bit more flexible.
### Create an Issue
1. Go to the Issues Tab
2. Click on `New issue`
3. In the title write "Add Instructions"
4. In the description use: `Add instructions to edit the HTML file to customize this for your own artwork.`
5. Click on `Assign yourself`
6. Add a `documentation` and `enhancement` label
7. Hit submit new issue
### Using AI to Create Documentation
AI Tools are great at helping you write documentation or code. 
1. Go back to your site's `code` tab
2. Click on the `local button` 
3. Click on the `Index.html` file.
4. Click on the `raw` file button
5. From the `file` menu in your browser hit the `save` button
6. Go to `chatgpt.com`
7. Drag the file to the Chat GPT window
8. Type in the following prompt: `Write some instructions using markdown to help people who want to use this code update it with their own images. Save it to a file`
### Updating the site
1. Go to the Issue you created to Add Instructions
2. Look for the `Create a branch` link on the sidebar
3. You can leave the name alone, but under what's next, choose open in codespace
4. Hit the `Create branch` button.
5. Hit the `Create codespace on <NAME>` button
### Using the Codespace
1. Create a `docs` folder
2. Upload the `update_instructions.md` file into the docs folder.
3. Open the README document.
4. Add the instructions at the end of the file
	1. ## Updating
	2. To update this with your own images, check out [these instructions](docs/update_instructions.md)
### Using Source Control
1. Switch to the source control icon on the left toolbar
2. Type in a commit message "updating docs"
3. Hit the `commit` button
4. Tell it to `always` stage and commit changes.
5. Click on the `Sync Changes` button, then click OK.
6. Optionally you can ask VSCode to periodically run `git fetch`
### Compare and Pull Request
When you come back to the site, you'll see an option to compare and pull request.
1. Hit the `Compare and pull request` button
2. Scroll down to review the changes.
3. Hit the `Create a pull request` button
4. Hit the `Merge pull request` button
5. Hit the `Confirm merge` button
6. Hit the `Delete branch` button
7. Optionally delete the codespace.

Now you can go back to the code page on the repo and see the changes. This will also automatically close the issue.

## Publishing GitHub Pages
If your page is an HTML document, you can easily publish the site using GitHub for free.
1. Go to the `Settings` tab on your repo.
2. Click on `Pages` on the left sidebar.
3. Under `Branch`, click on `None` and switch it to `main`
4. Leave `/root` as the destination and hit the save button.

After a few minutes `refresh` the page to get the URL of your published website.
Click on the link it generates.
## Adding Collaborators
You can add external collaborators to your site who will be able to help you or assist with your work. They will show up on projects, pull requests and issues.

1. Click on the `Settings` tab under the repo
2. Click on `Collaborators` on the left sidebar
3. Click on `Add people`
4. Feel free to add your teacher to your repo. You can use my email ray@planetoftheweb.com or @planetoftheweb. Make sure it looks like my profile photo. I have a couple of other accounts you can use if you want to test out making assignments to: **@jojohumphreys**, **@miguelmiles**, **@rogeliogreco** and **@noelmiles**. Try searching for them, the accounts all point to me.
## Adding Discussions
You can easily turn on discussions to engage with your users. They are very similar to issues, but have extra features.
### Exercise
Discussions are easy to add on through settings.
1. Click on the `Settings` tab under the repo
2. In the main project settings, scroll to the `Features` section
3. Click on **Discussions** to turn them on
4. Click on **Set up discussions**
5. Change or modify the title or description
6. Click on Start discussion

Once you turn on discussions, a new tab will appear at the top. People can comment on discussions. You can add labels, and there's a number of links on the sidebar. You can `lock the conversation`, `transfer this discussion` to another repo, `Edit the pinned discussion` or `unpin the discussion`, `Pin the discussion`, `create an issue from the discussion` and finally `delete discussion`.
