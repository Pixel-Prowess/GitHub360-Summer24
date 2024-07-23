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

## Teams
A way to assign roles to groups of people instead of individuals.
- Makes it flexible to manage what groups of people are able to do.
- Helpful when the individuals’ roles are in flux or people are coming in/out of teams.
- Teams can be @mentioned in communications (discussions, readme’s etc.)
- Teams can also have parent teams for ease when organizing.
- Teams have their own set of preferences and controls.

## Exercise
Create one or two teams. You'll need to have some people added to your organization. One team could be for the QA Team and another for Developers.

1. Click on the `Teams` tab
2. Hit the `New Team` button
3. Fill out some team details
4. Hit the `Create Team` button
5. Add people to your teams
6. Assign the team a role

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
Create a new project
1. Go to the project you just created
2. Edit 
3. Add several `Draft` tasks
4. Add `assignees` and `statuses`
5. Try adding more `columns`
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

Issues are how you connect draft tasks to items in your issues tab.
1. Convert a Task `to an Issue`
2. Assign it a `Repo`
3. Add issue related options
