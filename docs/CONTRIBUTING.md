# Contributing to NBility-Model

Thank you for considering contributing to the NBility-Model project! We appreciate your interest and look forward to your contributions. Follow the guidelines below to ensure a smooth and collaborative experience.


## Ways of Contributing

Contribution does not necessarily mean committing code to the repository. We recognize different levels of contributions, as shown below in increasing order of dedication:

1. **Testing and Feedback**
    * Test and use the model.
    * Provide feedback on the user experience.
    * Suggest new features.
2. **Validation**
    * Validate the model against your use-cases.
    * Share your feedback and experiences.
3. **Bug Reporting**
    * Identify and report bugs.
    * Provide detailed information to help us replicate and fix issues.
4.  **Documentation Improvement**
    * Enhance existing documentation.
    * Add new documentation to clarify and improve understanding.
5. **Model Development**
    * Feature Enhancements: Improve or add new features to the NBility codebase.


### Getting Started

A good place to start is to look at issues with the good first issue label, or to check the [NBility-Model project](https://github.com/orgs/NBility-Model/projects/3/views/1). These are beginner-friendly issues that are well-suited for new contributors.


## Using GitHub Issues for Bug Reports and Feature Requests

GitHub Issues is a powerful tool for tracking bugs, change requests, and feature requests. Here's how you can use it effectively to contribute to NBility-Model: 

1. **Submitting a Bug Report**

    * Navigate to the Issues tab.
    * Click on "New Issue" e.
    *Provide a descriptive title and detailed information about the bug, including steps to reproduce, expected behavior, and screenshots if applicable.

2. **Requesting a Feature**

    * Go to the Issues tab.
    * Click on "New Issue".
    * Describe the feature in detail, including the problem it solves and any potential implementation ideas.

3. **Submitting a Change Request**

    * Access the Issues tab.
    * Click "New Issue".
    * Provide a clear title and detailed description of the proposed change, including reasons for the change and any potential impacts.

4. **Tracking and Managing Issues**

    * Use labels to categorize and prioritize issues (e.g., bug, enhancement, documentation).
    * Assign issues to yourself or team members to indicate who is responsible for addressing them.
    * Comment on issues to provide updates, ask for more information, or discuss potential solutions.


### Example Issue Workflow

1. **Open:** The issue is created and needs to be addressed.
2. **In Progress:** The issue is currently being worked on.
3. **Review:** The issue is resolved and awaiting review.
4. **Closed:** The issue is resolved and closed after review.

Using [GitHub Issues](https://docs.github.com/en/issues) helps maintain a clear and organized workflow, ensuring that all contributions are properly tracked and managed.


## Using the NBility Model Project Planning Board

The [NBility-Model project Planning Board](https://github.com/orgs/NBility-Model/projects/3/views/1) is an essential tool for organizing and tracking the progress of tasks within the NBility-Model project. Here's how to use it effectively:

1. **Accessing the Board**
    * Navigate to the project's GitHub Planning Board to view all tasks and their statuses.
  
2. **Understanding Columns**
    * The board is divided into columns, each representing different stages of the workflow (e.g., Backlog, In Progress, Review, Done).
    * Tasks move from left to right as they progress through these stages.

3. **Creating and Assigning Tasks**

    * New tasks can be created by clicking the "New Issue" button. Provide a clear title and detailed description.
    * Assign tasks to yourself or others by using the assignee feature.

4. **Tracking Progress**

    * Update the status of tasks by dragging them to the appropriate column.
    * Use labels to categorize tasks by type (e.g., bug, feature, documentation).

5. **Collaborating and Communicating**

    * Comment on tasks to provide updates or ask for help.
    * Mention team members using @username to notify them of important updates.
  
## Example Workflow

1. **Backlog:** New ideas and tasks are added here.
2. **To Do:** Tasks that are ready to be worked on.
3. **In Progress:** Tasks currently being worked on.
4. **Review:** Completed tasks awaiting review.
5. **Done:** Completed and reviewed tasks.
   
Using the planning board helps keep the project organized, ensures transparency, and facilitates collaboration among contributors.


## Branching Strategy for Release Management

To ensure a stable and efficient release process, NBility-Model follows a branching strategy inspired by the [Stable Mainline Branching Model](https://www.bitsnbites.eu/a-stable-mainline-branching-model-for-git/) for Git. The following diagram illustrates the branching strategy:

![branch_strategie](images/Branch%20strategy.png)

Source diagram: <https://www.bitsnbites.eu/a-stable-mainline-branching-model-for-git/>


### Key Concepts

1. **Main Branch**

    * The main branch is always stable and contains the latest release-ready code.

2. **Feature Branches**

    * Feature branches are created from the master branch for developing new features or making changes. These branches are merged back into the master branch once the feature is complete and has passed review.

3. **Release Branches**

    * Release branches (release/vX.Y) are created from the main branch when preparing for a new release. This allows for final testing and bug fixing without disrupting ongoing development.
    * Release candidates (vX.Y.0-rc1, vX.Y.0-rc2, etc.) are tagged in the release branch as needed.

4. **Hotfixes and Quick Fixes**

    * Critical fixes can be made directly on the release branch and merged back into the main branch. These fixes can also be cherry-picked into other branches if necessary.

### Workflow
1. **Development**

    * Create a feature branch from main.
    * Develop and test the feature in the feature branch.
    * Merge the feature branch back into main after review and testing.

2. **Release Preparation**

    * Create a release branch from main.
    * Perform final testing and make any necessary fixes in the release branch.
    * Tag release candidates as needed (vX.Y.0-rc1, vX.Y.0-rc2, etc.).

3. **Release**

    * Merge the release branch back into main once it is stable.
    * Tag the final release (vX.Y.0).

4. **Hotfixes**

    * Apply critical fixes directly to the release branch.
    * Merge these fixes back into main and any active feature branches as needed.

This branching strategy ensures a stable mainline while allowing for efficient development, testing, and release management.


## How to Contribute to the Documentation

### Using the Markdown formatted text

For all documentation, the NBility model uses Markdown. Markdown is a lightweight markup language that allows you to add formatting elements to plaintext documents.

For more information on the Markdown format, see [Getting Started with Markdown](https://www.markdownguide.org/getting-started/)


### Submitting Contributions

Contributions for contributors should be submitted as GitHub pull requests. See [Creating a pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) if you're unfamiliar with this concept. When submitting a pull request, please ensure:

Once the Pull Request has been reviewed and accepted, the feature branch can be merged with the main repository. By doing so, the changes in the feature branch are committed to the main branch.


## How to Contribute to the Model

### Collaboration - Feature Branches

NBility-Model provides the possibility for users to collaborate on modeling and working on the same repository. Depending on the need, multiple feature branches may be created. See this article on how to create a feature branch. Each user with the appropriate permissions can create a feature branch from the main branch and provide permission to other users who will work on this feature branch.

Feature branches exist parallel to the main branches. Users can make changes and commit them to feature branches. They are then visible to all other users. Feature branches provide an effective way for collaboration. Users can work on various aspects of an architecture model and share the progress with each other for review and comments without changing or affecting the main repository.

### Overview of Collaboration

After opening [Archi](https://www.archimatetool.com/), from the menu, choose _Collaboration_ and then click _Toggle collaboration_. This will open the collaboration workspace showing all repositories where multiple users are collaborating. Clicking on a repository will show all feature branches and the users who created these branches, as shown in Figure 1 below.

![coArchi-github-settings](images/Fig%201%20Collaboration.png)
Fig. 2

### Consistency in Commits to Main Branch

It might occur that users, while working on their own branches, make changes that conflict. For such cases, Archi has a conflict resolution mechanism wherein for every conflicting change, the user is asked to specify the change in the model they would like to keep, and which changes can be omitted. By doing so, consistency is ensured in the main architecture repository.


### Follow the NBility model design guidelines

NBility model adheres to generic design guidelines. Every adjustment and/or expansion should conform to these guidelines. These guidelines consist of:

* NBility metamodel
* Naming conventions
* Model explenation / design choices
* Consistency rules

For more information on these guidelines, see [GUIDELINES.md](GUIDELINES.md)


### Submitting Contributions

Contributions for contributors should be submitted as GitHub pull requests. See [Creating a pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) if you're unfamiliar with this concept. When submitting a pull request, please ensure:

* Your code adheres to the project's [design guidelines](GUIDELINES.md). 
* You have tested your changes thoroughly.
* You have updated any relevant documentation.

Once the Pull Request has been reviewed and accepted, the feature branch can be merged with the main repository. By doing so, the changes in the feature branch are committed to the main branch.


## Getting Help

If you need help or have any questions, feel free to open an issue on GitHub, and we'll do our best to assist you.

We appreciate your contributions and efforts in making NBility-Model better!

Happy coding!
