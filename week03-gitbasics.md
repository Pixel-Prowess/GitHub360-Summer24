## Collaborators Review
Let's start by going over how collaborators work, although it's something we've covered before.

Collaborators are a simple way to add members to your repos and give them access to files and projects. This also works in a team environment.

Collaborators will have access to:

1. Read  
    View repository contents. View and comment on issues and pull requests. Clone the repository.
    
2. Triage  
    Collaborators can manage issues and pull requests, request reviews, close or reopen issues and pull requests.
    
3. Write  
    They can push changes to the repository, create and manage branches, merge pull requests and manage code settings.
### Exercise
1. Find a repository
2. Go to `settings`
3. Click on the `collaborators` tab on the left
4. Hit the `Add people` button.
5. Search for another user by username. You may use your teacher's account `planetoftheweb` if you need to invite someone. You can also use: **jojohumphreys**, **miguelmiles**, **rogeliogreco** and **noelmiles**.

---
## Organizations
Businesses and open source project can collaborate across a group of repos. You can create organizations [for free](https://github.com/organizations/plan) with certain limits. 

Enterprise accounts allow you to create multiple organizations, Organizations can have multiple repositories.

You can add codespaces or copilot as add ons to free organizations. They cost $4/user/month, or $21/user/month for enterprise accounts.

- Free for open source projects with limits
- Organizations allow you to group repositories.
- You can organize members into different teams
- Team members can have different permissions.
- Enterprise accounts allow you to create multiple organizations and multiple repos in the organizations.
### Exercise
1. [Create](https://github.com/organizations/plan) your own organization.
2. Connect it to your personal account
3. Accept the Terms of service
4. Hit the next button

---
## Organization Options
Organizations have their own tabs and preferences.
- **Overview** shows you a README file from one of two repositories.
	- For the public, create a public repo called .github, add a file in that repo under /profile/README.md
	- For your members, create a private repo named .github-private and a file called /profile/README.md
- Organizations can publish **Packages**, which are special projects for modules generally used in the open source community.
- Organizations can also have their own **discussion boards** tied to a specific repo.
- **Teams** can give members different permissions.
- **People** with access to your repo are stored in a single place.
- **Settings** show you additional options.**
### Exercise
Add a public repo with some welcome text.
1. Create a new repo called `.github`
2. Add a file in the repo called `/profile/README.md`
3. Here's some [sample text](https://gist.githubusercontent.com/planetoftheweb/952c1293e12dfe685b8f5a69fd54039d/raw/cc95b05ca41a9c850b10782fbb997cfac6aaa7a8/public.md) you can use.
### Exercise
Add a private repo with some welcome text.
1. Create a private repo named `.github-private`
2. Create a file called `/profile/README.md`
3. Here's some [sample text](https://gist.githubusercontent.com/planetoftheweb/ed83fc2924ff4f9fa7287e7354de1167/raw/8765660d8a4ece3d3b426ecabd9d29e901fdee3a/privatewelcome.md) you can use.

---
## Organization Discussions

Organizations can also have discussions.
- They require a source repository that will host the discussions. (Can be your `.github-private` member repository.
- All discussions on the source repository will be surfaced to the organization Discussions tab.
- Permissions from the repository will be applied to the organization Discussions. By default, all members of the organization will be able to create and comment on discussions.
- Members can share updates or ask questions to the entire organization.

### Exercise
Add a discussion to your organization repo.
1. Click on the link on the sidebar to add a discussion repo to the organization.
2. Choose the `.github-private` repository as the default repo.
3. Create a single post.

---
## People
The People tab allows you to add members and manage collaborators to your repository.
- Invite members as usual.
- You can export the data for your members to a CSV or a JSON file.
- Members can have base permissions under `/settings/member_privileges`
- You can also see the `outside collaborators` that have been granted access to specific repos.
- The permissions of collaborators are limited to the repos they have access to, whereas `members` have the same permissions for the whole repo.
- You can `manage invitations` and see pending collaborators as well.
### Exercise
Invite a few members to your repository.
1. Click on the people tab inside your organization
2. Click on the invite member button
3. Add people to your organization
4. Search for users by username. You may use your teacher's account `planetoftheweb` if you need to invite someone. You can also use: **jojohumphreys**, **miguelmiles**, **rogeliogreco** and **noelmiles**.

---
## Organization Roles
Roles control the access people or teams get within the organization.
- All-repository read. Basic role. Gives read access to all repos without management capabilities
- All-repository write. Allows users to push changes, manage issues and pull requests, and set repository milestones without full administrative rights.
- All-repository triage. Allows project managers to manage issues and pull requests without write access to the code.
- All-repository maintain. Grants more extensive project management permissions, including settings, protected branches, metadata without full admin rights.
- All-repository admin. Full control including settings, users, security alerts, protected branches, and repository rules
- Under settings/repository roles, you can also see individual repo roles and if you have an enterprise account, create custom roles.
### Exercise
Give an individual a triage role.
1. Go to the `people` tab
2. Find a user without any roles
3. Click on the `0 roles` link
4. Click on `New role assignment` button
5. Choose the `All-repository triage` role

---
## Member privileges
These let you control everything members are able to do by default as members.
- **Base permissions**. Lets you choose the default permission
- **Repository creation**. If they’re able to create public or private repos.
- **Forking**. Enable forking of private repos.
- **Discussions**. If user can create discussions.
- **Projects base permissions**. The role for projects.
- **Pages creation**. Can they create pages?
- **Integration**. Can they allow external integrations.
- **Admin permissions**. Other permissions like if they are allowed to change issue visibility, delete or transfer repos, delete issues.
- **Team Creation**. Can the member create teams.

---
## Teams
A way to assign roles to groups of people instead of individuals.
- Makes it flexible to manage what groups of people are able to do.
- Helpful when the individuals’ roles are in flux or people are coming in/out of teams.
- Teams can be @mentioned in communications (discussions, readme’s etc.)
- Teams can also have parent teams for ease when organizing.
- Teams have their own set of preferences and controls.
### Exercise
Create one or two teams. You'll need to have some people added to your organization. One team could be for the QA Team and another for Developers.

1. Click on the `Teams` tab
2. Hit the `New Team` button
3. Fill out some team details
4. Hit the `Create Team` button
5. Add people to your teams
6. Assign the team a role

---
## Projects
Projects are a way to organize and track issues with different views. Multiple tabs
- You can get started with templates like Team Planning and Feature Release or choose one of the three manual options.
- You can also create your own template.
- Projects are never deleted directly, just closed. To delete a project, go to the project settings menu, then go to the danger zone and delete.
- There are three main project types:
	- **Table**. This view gives a spreadsheet style view with customizable fields
	- **Board**. The traditional Kanban board style way to organize things by column you can move tasks through.
	- **Roadmap**. This one is more of a timeline view for project managers.
### Exercise
Create a new project
1. Go to the `Projects` tab in your Organization or personal account
2. Click on `New Project`
3. Choose the `table` option
4. Give the project a name
5. Hit the `Create project` button
6. Edit the project name and description.

---
## Tables
Powerful spreadsheet template. You can filter, sort and group. You can also add your own columns and your own tabs.
- At the top is the Project Title. Click to enter a title, description and a README.
- Underneath the title is the tabs. You start with one tab named View 1. You can click on the name of the tab to change it.
- New views can be of any other type or you can make a copy of the existing view.
- To add items you can use control-space or just click on the table or the plus sign.\
- A task is a designated as a draft item before it gets converted to an issue. You can use these to plan out your tasks in a project.
- You can add assignees (the people in your project) and one of three statuses: Todo, In Progress and Done.
- Once you create a task, you can click on it’s name to see the details.
- You can use # to tie the task to a repo
### Exercise
Add table views to your project.
1. Go to the `project` you just created
2. Click on the `title` to see the Project Settings
3. Explore some of the fields available for modifying your project information.
4. Add a Short description as well as some content to the READ ME section.
5. Hit the **Save changes** button.
### Exercise
Take a look at the more options in Project settings
1. Click on the `Manage access` tab
2. Look at the options available there
3. Pay close attention at the people listed under the **Manage access** section
### Exercise
Create draft items
1. Click on the first tab under the project title.
2. Change the name to something like `table view`
3. Click on the triangle dropdown to see additional options
4. In the `Title column` click on the first item to add a new draft item
5. In the `Assignees` column,  click to pick one or more assignees to your draft item.
6. Click on the Status column and choose `Todo` as the status
7. Add a series of additional draft items

---
## Issues
You can convert tasks to issues for some additional capabilities.
- Converting to Issues requires that you specify a repo. 
- When you convert, the Issue gets a number and clicking on the title will give you an issue form.
- Your columns can now include labels and other things.
- When you modify the columns, notice the save button is now available. If you save, it will update the view to include these columns.
- You can also add a new view with a different set of columns
- You can use the filter section to modify specific views and do things like create a view with just tasks assigned to you.
- You can add a totally new custom field.
### Exercise
Convert draft items to issues
1. Click on the `title` of a draft item to see the sidebar window.
2. On the right, click on the `Convert to issue` link
3. In the `dropdown`, choose an `existing repository` to assign this to
4. Look at the `additional options` available, which are common to issues.
### Exercise
Add new columns to table views.
1. Go back to the `main table` view
2. On one of your `Issues`,  look for the `plus (+)` sign at the end of the current columns
3. Click on the `Plus` button
4. Choose `Labels` from the list
5. On the new Labels column, look for the `triangle dropdown`.
6. Click on it to select labels for one of the issues
### Exercise
Create a new field.
1. Click on the  plus (+) sign at the end of the current columns again.
2. Click on + New field
3. Create a field called Website URL
4. Add a website URL to one of your Issues
### Exercise
When you change a view tab, you can save the changes to the table view
1. Look in current tab for the blue dot, showing that you've made changes to the view.
2. Look in the right next to the filter text box and hit the save button to save your new view
3. Click on the name of the current view and change it to `Table view`
### Exercise
Create a custom view showing the issues you're assigned to.
1. Make sure that at least of one of the issues you created, you have made yourself the `assignee`.
2. Next to the tabs under the title, look for a `New view` link.
3. From the dropdown choose `Table`
4. Click on the tab to rename your view, call it `Assigned to me`
5. Under the Filter section, type in `assignee:`
6. From the dropdown, choose `your account`.
7. Look for the save button to the right of the filters and click `Save`.

---
## Boards
Boards allow you to move tasks in a two dimensional space that allows you to visually see different status.
1. Boards show the status of your tasks.
2. The default statuses are: Todo, In Progress and Done, but you can also add custom statuses.
3. These are the oldest types of project views and they are inspired by Kanban boards from the agile methodology.
4. You can easily move tasks from one column to another as you work through a project.
5. The moves are logged and tracked into your project’s history.
6. Kanban boards can still be filtered so that you can create a view with only your order.
7. Each column has a set of options under … that lets you archive, delete, set a limit for how many items show, 
### Exercise
Create a new Boards style tab
1. In the tabs, click on the `+ New view` option
2. Choose the `Board` option from the dropdown
3. Rename the board by clicking on the tab title, call it `Kanban`
4. If you added statuses to your issues in table view, they should show up here.

### Exercise
Modify the status of one of the issues
1. `Click and drag` one of the `issues` from an existing column to another one
2. `Click` on a different `tab` to see the status has changed there as well.
3. Click back on the `Kanban tab.`
### Exercise
Add a new column to the board view
1. To the right of all columns look for the `plus (+)` button.
2. Click on that button, then choose `New Column`
3. On the pop-up Type in `Backlog`, then optionally choose a color not in one of the current tabs.
4. Click `Save`
### Exercise
Change the position of the column, 
1. Click on the `title` of the `column` and drag
2. You should see a `thick blue` border
3. Let go to move the column
4. Move one of the issues into the new column
5. Click the `Save` button to the right of the filters to save the changes to the view.

---
## Roadmap
These views let you see a timeline view for when tasks are related to at least one date or iteration field.
- The easiest would be a Start date and End date.
- To create a timeline, you can click and drag
- These fields are added as custom fields.
- You can show different markers, sort, look at the project by month quarter or year.
### Exercise
Create a new Timeline style tab
1. In the tabs, click on the `+ New view` option
2. Choose the `Roadmap` option from the dropdown
3. Rename the Roadmap by clicking on the tab title, call it `Timeline`
### Exercise
A roadmap requires having at least one date field. Let's add two new fields.
1. To the right of the roadmap, under the filter area, look for the `Date fields` dropdown.
2. Click on `New field`
3. Call the field `Start`
4. Choose `Date` as the field type.
5. Click on save

### Exercise
Finish setting up the timeline
1. Repeat the process for another field called `End`
2. Click on the `Date fields` dropdown again
3. Choose the new `Start` field under the heading `Start date`
4. Choose the new `End` field under the heading `End date`
### Exercise
Add a start and end date to some of the issues.
1. Under the range of dates, click on a start date next to an issue
2. Once you see the end date, click and drag to set the end date.
3. Continue setting an end date for other issues

---
## Status Update
You can create short messages that help communicate the status of the project.
- These messages will update your users to let them know the status of the project
- You can add status types of: `Inactive`, `On track`, `At risk`, `Off track` or `Complete`
- You can add a Start date and a Target date
### Exercise
Create a Status message
1. To the right, on top of the filters, look for the `Add status update`
2. Under the Status button choose one of the tags:  `Inactive`, `On track`, `At risk`, `Off track` or `Complete`
3. Click on the `Start date` button and choose a date
4. Click on the `Target date` button and choose a date
5. Type in a Description and choose the `Save update` button
6. Click on the close button at the top right to close the view.
7. Notice the status should now mirror your tag as (i.e. 'On track')

---
## Insights
Create graphs and charts based on the data on a project.
- You can create different visuals based on the data for the project
- You can create: bar, column, line, stacked area, stacked bar, stacked column.
- Control the x or y axes, group by the status 
### Exercise
Take a look at insights for your project.
1. On top of the filters look for the insights icon next to the status
2. Click on insights.
3. You should be able to see a simple status chart.
4. Click on configure to see a list of options to control the `layout`, `x or y axes` and how to `group the data`.
### Exercise
Add another chart
1. On the left under `Custom charts`
2. Click on the `New chart` button.
3. Configure and customize this new chart with options from the configure section.
4. To rename a chart, click on the pencil icon to the left of the `configure` button.
