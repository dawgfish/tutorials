******************
Lab - GitHub
******************

Introduction:
*************
GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

This lab teaches you GitHub essentials like repositories, branches, commits, and Pull Requests. You’ll create your own Hello World repository and learn GitHub’s Pull Request workflow, a popular way to create and review code.

No coding necessary
===================
To complete this tutorial, you need a GitHub.com account and Internet access. You don’t need to know how to code, use the command line, or install Git (the version control software GitHub is built in).

.. note:: Open this guide in a separate browser window (or tab) so you can see it while you complete the steps in the tutorial.

Create a Repsitory:
*******************
- In the upper right corner, next to your avatar or identicon, click + and then select New repository.
- Name your repository hello-world.
- Write a short description.
- Select Initialize this repository with a README.

[IMAGE]

Create a Branch:
****************
Branching is the way to work on different versions of a repository at one time.

By default your repository has one branch named master which is considered to be the definitive branch. We use branches to experiment and make edits before committing them to master.

When you create a branch off the master branch, you’re making a copy, or snapshot, of master as it was at that point in time. If someone else made changes to the master branch while you were working on your branch, you could pull in those updates.

This diagram shows:

- The master branch
- A new branch called feature (because we’re doing ‘feature work’ on this branch)
- The journey that feature takes before it’s merged into master

[IMAGE]

Have you ever saved different versions of a file? Something like:

- story.txt
- story-joe-edit.txt
- story-joe-edit-reviewed.txt

Branches accomplish similar goals in GitHub repositories.

Develoeprs use branches for keeping bug fixes and feature work separate from the master (production) branch. When a change is ready, developers will merge their branch into master.

To create a new branch:

- Go to your new repository hello-world.
- Click the drop down at the top of the file list that says branch: master.
- Type a branch name, readme-edits, into the new branch text box.
- Select the blue Create branch box or hit “Enter” on your keyboard.

.. figure:: https://guides.github.com/activities/hello-world/readme-edits.gif
