---
title: "Creating workspaces in Postman"
updated: 2021-09-30
contextual_links:
  - type: section
    name: "Additional resources"
  - type: subtitle
    name: "Videos"
  - type: link
    name: "Creating a Workspace | Postman Level Up"
    url: "https://youtu.be/I10RCvMbPi0"
  - type: link
    name: "Use Collection and Workspace Templates"
    url: "https://youtu.be/QAIH1D203Wg"
  - type: subtitle
    name: "Blog posts"
  - type: link
    name: "Solving Problems Together with Postman Workspaces"
    url: "https://blog.postman.com/solving-problems-together-with-postman-workspaces/"
  - type: link
    name: "Movember Foundation"
    url: "https://www.postman.com/case-studies/movember-foundation/"
  - type: section
    name: "Next steps"
  - type: link
    name: "Using and managing workspaces"
    url: "/docs/collaborating-in-postman/using-workspaces/managing-workspaces/"

warning: false

---

Workspaces enable you to organize your Postman work and collaborate with teammates. You can group your projects together, with workspace acting as the single source of truth for related APIs, collections, environments, mocks, monitors, and other linked entities. By collaborating in a workspace, your edits sync with your team in real time.

<img alt="Workspaces selected" src="https://assets.postman.com/postman-docs/v10/workspace-overview-switcher-selected-v10-2.jpg"/>

With a [Postman account](/docs/getting-started/postman-account/) you can create various types of workspaces:

* **Personal** - Personal workspaces are visible to you. If you're on an Enterprise team, [Super Admins](/docs/collaborating-in-postman/roles-and-permissions/#team-roles) will also have access to any personal workspaces created within the team.
* **Private** - Private workspaces are visible to you and to any team members you invite to them ([Professional and Enterprise plans](https://www.postman.com/pricing)).
* **Team** - Team workspaces enable you to share projects with collaborators and manage access to them within your team.
* **Partner** - Invited team members and [partners](/docs/collaborating-in-postman/using-workspaces/partner-workspaces/) can access Partner Workspaces ([Enterprise Ultimate plans only](https://www.postman.com/pricing)).
* **Public** - [Public workspaces](/docs/collaborating-in-postman/using-workspaces/public-workspaces/) enable you to collaborate on entities with anyone across the world.

By adding an element to a workspace, collaborators with access to the workspace will also be able to access the element by default with read permissions. You can [configure access settings](/docs/collaborating-in-postman/roles-and-permissions/) for the workspace on an individual basis to give permissions depending on the account.

Workspaces can also create visibility for the projects within a team, as collections in a workspace are visible to all team members with access to the workspace.

_Workspace as an element_ represents a whole container where being an Admin gives you full access to the workspace. This works like the inheritance property where you will have Editor access to all the elements within that particular workspace.

> For Postman Professional and Enterprise teams, a private workspace is a team workspace that's visible to the user who created it, plus team members who have been invited to join it. Private workspaces let teams restrict access to APIs, collections, environments, mocks, and monitors that are relevant to a particular group.

## Contents

* [Creating a new workspace](#creating-a-new-workspace)
* [Creating workspaces with a template](#creating-workspaces-with-a-template)
* [Next steps](#next-steps)

## Creating a new workspace

1. To create a new workspace, select **Workspaces** in the header, then select **Create Workspace**.

    <img alt="Create new workspace" src="https://assets.postman.com/postman-docs/v10/workspace-switcher-v10.14.jpg" width="300px"/>

1. Use the visibility menu to choose a __Personal__, __Private__, __Team__, __Partner__, or __Public__ workspace.

    <img alt="Create new workspace" src="https://assets.postman.com/postman-docs/v10/create-workspace-v10.jpg" width="500px"/>

1. Select **Create Workspace** and Postman will open your new workspace. You can add elements to the workspace. Select __Invite__ in the Postman header to add other users to the workspace.

To create a new workspace, you can also select __New__ in the sidebar, then select __Workspace__ and follow the same steps.

<img alt="Create new workspace" src="https://assets.postman.com/postman-docs/v10/create-new-workspace-v10.jpg" width="500px"/>

You can also create a new workspace in the [Workspaces dashboard](https://app.getpostman.com/dashboard). Select **Create workspace** and follow the same steps.

![Create new workspace dashboard](https://assets.postman.com/postman-docs/v10/create-new-workspace-dashboard-v10.jpg)

## Creating workspaces with a template

You can use workspace templates to help you set up a new workspace. Workspace templates are available for a variety of common use cases:

* API Demos
* Engineering Onboarding
* API Testing
* Security
* Incident Response
* Infrastructure

When you apply a workspace template, it will populate the workspace description with an introduction and information to help you get started. Each workspace template also includes sample collections that you can use and change as needed.

To use a template, [create a new workspace](#creating-a-new-workspace) or open a newly created workspace. In the workspace overview, select from the available templates under **Use a template to quickly set up your workspace** or select **More templates** to view all of the available options. You can select the template you'd like to use, then select **Use Template**.

<img alt="Select workspace template" src="https://assets.postman.com/postman-docs/v10/workspace-templates-api-testing-v10.14.jpg"/>

## Next steps

After you create a workspace, you can use the workspace to collaborate with your team.

* To learn more about what you and your team can do with workspaces, go to [Managing workspaces](/docs/collaborating-in-postman/using-workspaces/managing-workspaces/).
* You can also use your workspace [activity feed](/docs/collaborating-in-postman/using-workspaces/changelog-and-restoring-collections/) to keep up to date with progress on the projects within it.
