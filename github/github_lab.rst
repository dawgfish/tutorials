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

Create a Repository:
*******************
- In the upper right corner, next to your avatar or identicon, click + and then select New repository.
- Name your repository hello-world.
- Write a short description.
- Select Initialize this repository with a README.

.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/github/image2.png

Create a Branch:
****************
Branching is the way to work on different versions of a repository at one time.

By default your repository has one branch named master which is considered to be the definitive branch. We use branches to experiment and make edits before committing them to master.

When you create a branch off the master branch, you’re making a copy, or snapshot, of master as it was at that point in time. If someone else made changes to the master branch while you were working on your branch, you could pull in those updates.

This diagram shows:

- The master branch
- A new branch called feature (because we’re doing ‘feature work’ on this branch)
- The journey that feature takes before it’s merged into master

.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/github/image1.png

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

.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/github/image10.gif

Now you have two branches, master and readme-edits. They look exactly the same, but not for long! Next we’ll add our changes to the new branch.

Make and Commit Changes:
************************
Bravo! Now, you’re on the code view for your readme-edits branch, which is a copy of master. Let’s make some edits.

On GitHub, saved changes are called commits. Each commit has an associated commit message, which is a description explaining why a particular change was made. Commit messages capture the history of your changes, so other contributors can understand what you’ve done and why.

Make and commit changes:

- Click the README.md file.
- Click the  pencil icon in the upper right corner of the file view to edit.
- In the editor, write a bit about yourself.
- Write a commit message that describes your changes.
- Click Commit changes button.

.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/github/image3.png

These changes will be made to just the README file on your readme-edits branch, so now this branch contains content that’s different from master.

Open a Pull Request:
********************
Nice edits! Now that you have changes in a branch off of master, you can open a pull request.

Pull Requests are the heart of collaboration on GitHub. When you open a pull request, you’re proposing your changes and requesting that someone review and pull in your contribution and merge them into their branch. Pull requests show diffs, or differences, of the content from both branches. The changes, additions, and subtractions are shown in green and red.

As soon as you make a commit, you can open a pull request and start a discussion, even before the code is finished.

By using GitHub’s @mention system in your pull request message, you can ask for feedback from specific people or teams, whether they’re down the hall or 10 time zones away.

You can even open pull requests in your own repository and merge them yourself. It’s a great way to learn the GitHub Flow before working on larger projects.

+--------------------------------------------+-------------------------------------------------------------------------------------------------+
|             STEPS                          |                             SCREENSHOT                                                          |
+--------------------------------------------+-------------------------------------------------------------------------------------------------+
|                                            |                                                                                                 |
|Click the Pull Request tab, then from the   |                                                                                                 |
|Pull Request page, click the green New.     |.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/github/image5.gif        | 
|pull request button.                        |                                                                                                 |
+--------------------------------------------+-------------------------------------------------------------------------------------------------+
|In the Example Comparisons box, select the  |                                                                                                 |
|branch you made, readme-edits, to compare   |                                                                                                 |
|with master (the original)                  |.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/github/image6.png        | 
|master (the original)                       |                                                                                                 |
+--------------------------------------------+-------------------------------------------------------------------------------------------------+
|Look over your changes in the diffs on the  |                                                                                                 |
|Compare page, make sure they’re what you    |                                                                                                 |
|want to submit.                             |.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/github/image7.png        |
|                                            |                                                                                                 |
+--------------------------------------------+-------------------------------------------------------------------------------------------------+
|When you’re satisfied that these are the    |                                                                                                 |
|changes you want to submit, click the big   |.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/github/image8.png        |
|green Create Pull Request button.           |                                                                                                 |
|                                            |                                                                                                 |
+--------------------------------------------+-------------------------------------------------------------------------------------------------+
|                                            |                                                                                                 |
|Give your pull request a title and write a  |.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/github/image9.png        |
|brief description of your changes.          |                                                                                                 |
|                                            |                                                                                                 |
+--------------------------------------------+-------------------------------------------------------------------------------------------------+


When you’re done with your message, click Create pull request!

.. note:: You can use emoji and drag and drop images and gifs onto comments and Pull Requests.

Merge Pull Request
******************
In this final step, it’s time to bring your changes together – merging your readme-edits branch into the master branch.

- Click the green Merge pull request button to merge the changes into master.
- Click Confirm merge.
- Go ahead and delete the branch, since its changes have been incorporated, with the Delete branch button in the purple box.

.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/github/image4.png

Celebrate!
==========
By completing this lab, you’ve learned to create a project and make a pull request on GitHub! :tada: :octocat: :zap:

Here’s what you accomplished in this lab:

- Created an open source repository
- Started and managed a new branch
- Changed a file and committed those changes to GitHub
- Opened and merged a Pull Request
