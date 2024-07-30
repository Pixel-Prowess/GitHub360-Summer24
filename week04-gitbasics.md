## Milestones
Milestones give you a way to create targets for your development projects. A group of tasks can be assigned to milestones and you can check the progress towards your milestones.

- Unlike projects, milestones are tied to your repos, not your projects.
- They are accessible to your projects though.
- Available from the Issues or Pull Requests page.
- Use the `New milestone` button
- You can also create a milestone directly on any issue page.

### Exercise
Create a `Project Launch` milestone to a repo
- Go to your project repo.
- Click Issues or Pull requests
- Click on the `New milestone` button
- Make the title `Project launch`
- Under `Due date`, add a due date

### Exercise
Add milestones to your issues
- Go back to the `Issues` Tab
- Find or create an issue and `click to open` it.
- Look for the `milestone section` on the right hand side and click on the `gear icon`.
- Click on the `issue` you created.
- Find other issues and `assign them` to the milestone
- `Close issues` to see how it affects the milestones.

---
## Releases
A release lets you lock in a version of a project It creates a page with release notes and lets people allowing download zipped versions of your projects.
- Releases use a Git feature called Tags
- The tag names should start with the letter `v`, then a series of `version numbers`  according to the [Semantic Versioning](https://semver.org/) standard.\
- AI can look through your `merged pull requests` and `write release notes`.
### Exercise
Create a new release for one of your projects.
1. Go to a `repository`
2. On the right hand side look for the `Releases` section
3. Click on `Create a new release`.
4. Under `Choose a tag`  type in `v1.0.0`
5. Click on `Create new tag`
6. Click on the `Generate release notes`
7. Hit the `Publish release` button

---
## Forking
Forks are a way of creating an alternate version of an existing project.
- Common for modifying a 3rd party project
- You can make changes that your work get added to the original project
- Create a pull request to suggest the changes
- Members can discuss and accept external changes
- Your work can be merged into the main project
### Exercise
Create a fork of a project.
- Go to [this project ](https://github.com/planetoftheweb/demo-forking-01)
- Click on the `fork` button
- Choose an `owner`
- Git the forked repository a `name`
- Click on the `Create fork` button
### Exercise
Modify the existing fork
- On the fork you just created, go to the `code  tab`
- Scroll down to the `pencil button` on the README file.
- Add "completed by `Name`" under the heading Completions
- Hit the `Commit changes` button
- On the Pop-up, also hit the `Commit changes` button
### Exercise
Contribute your change to the original
- On the code page, click on the `Contribute` dropdown
- Click on the `Open pull request` button
- Add a title "Adding `<yourname>` to the project"
- Hit the `Create pull request` button

---
## Copilot Workspace
This paid feature allows you to use AI to steer and help you accomplish a task.
- Based on Issues
- Must be on a paid plan
- Creates a plan of action from an Issue
### Exercise
If available to you, create a gitHub WorkSpace
- Create a new `Issue`
Add the following 
```
I'd like to add a dark mode option to this site.

- [ ] Create a button to toggle light or dark mode in the menu
- [ ] Add the script necessary to toggle between modes
- [ ] Modify the styles necessary
```

- Click on the `Open in Workspace` button on the right sidebar.
- Take a look at `the plan` to see the proposed changes
- You can `manually update` the plan

### Exercise
Modify the issue to regenerate the plan
- Click on the `pencil icon` to modify the issue
- Add an item `- [ ] Update the README file so it includes this feature`
- Hit the `Update specification` icon
- You can also click on `View references` to take a look at files, or even modify them

### Exercise
Review the plan 
- Hit the `Generate plan` button
- Review the proposed changes
- Hit the `Implement selected files` button
- The AI will attempt to `generate the code` for you.
- `Review the changes` and make modifications to files
- Hit the `create pull request` button
- Hit the `continue` button

### Exercise
Take a look at the changes suggested by the AI
- Go to the `pull requests` tab
- Under the `code` button, click on the `Codespaces` tab
- Click `Create codespace` on the branch
- Preview the changes
- Merge pull requests

---
## Actions
Actions provide a way to automate processes in your projects.
- There are `pre-built` actions in the [GitHub Marketplace](https://github.com/marketplace?type=actions)
- Actions use the [YAML format](https://yaml.org/) with built-in aides
- If you have a project built with GitHub Pages it runs as an action
- Actions can run scripts to process files
- You can `publish an action` to the Marketplace as long as you have a `release`
- You can take a look at some of my published actions: [Podcast Generator](https://github.com/marketplace/actions/podcast-generator) and [Copy to Branches](https://github.com/marketplace/actions/copy-to-branches-action)
### Exercise
Incorporate the [Auto-assign new issues](https://github.com/marketplace/actions/auto-assign-issue) action into a project.
- Go to the `Actions` tab
- Click on `New workflow`
- Click on `set up a workflow yourself`

```
name: Issue assignment

on:
    issues:
        types: [opened]

jobs:
    auto-assign:
        runs-on: ubuntu-latest
        permissions:
            issues: write
        steps:
            - name: 'Auto-assign issue'
              uses: pozil/auto-assign-issue@v2
              with:
                  assignees: planetoftheweb
                  numOfAssignee: 1
                  allowSelfAssign: true
```

- Paste the code into `text box`
- Make sure you update `<accountname>` with your own github account
- `Commit changes` to activate the action
- Create a `new Issue`
- Switch back to the Actions tab to `watch the action run`.
- Look at the issue again `when finished`.
- Notice the issue has been updated with the proper assignee.
