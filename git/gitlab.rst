*************
Lab - Git
*************


Introduction:
*************
Git is a distributed revision control and source code management system with an emphasis on speed. Git was initially designed and developed by Linus Torvalds for Linux kernel development and is a free software distributed under the terms of the GNU General Public License.

This lab guides users how to use Git for project version control in a distributed environment while working on source code and non-source code projects.

The Lab will help beginners learn the basic functionality of Git version control system. After completing this lab, participants will have a moderate level of expertise in using Git version control system to build upon.

This lab assumes participants are going to use Git to handle various projects. It's good to have some exposure to software development life cycle and working knowledge of application development but not required.

Workflows:
**********
General workflows are as follows:

- You clone the Git repository as a working copy.
- You modify the working copy by adding/editing files.
- If necessary, you also update the working copy by taking other developer's changes.
- You review the changes before commit.
- You commit changes. If everything is fine, then you push the changes to the repository.
- After committing, if you realize something is wrong, then you correct the last commit	and push the changes to the repository.
- Shown below is the pictorial representation of the work-flow.


.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/git/image2.png

Basic Concepts:
***************
Version Control System (VCS) is software that helps software developers work together and maintain a complete history of their work.

Listed below are the functions of a VCS:

- Allows developers to work simultaneously.
- Does not allow overwriting each other’s changes.
- Maintains a history of every version.

Git Advantages:
***************

Open Source
===========
Git is released under GPL’s open source license. It is distributed freely. You can use Git to manage projects without licensing costs. Because it's open source, you can download the source code and make changes that have affinity with your project requirements.

Fast and Compact
=================
Most of the operations are performed locally providing benefit in terms of speed. Git doesn't depend on a central server; which is why there's no need to interact with remote server(s) for every operation. Git's core is written in C, which avoids runtime overhead associated with other high-level (interpreted) languages. Git mirrors an entire repository, the size of the data on the client side is small, illustrating the efficiency of Git at compressing and storing data on the client side.

Implicit backup
================
The chances of losing data are reduced because there are multiple distributed copies. Data present on any client mirrors the repository so it can be used in the event of data corruption or disk crash

Security
=========
Git uses a widely adopted cryptographic hash function called secure hash function (SHA1), to name and index objects within its database. Every file and commit is check-summed and retrieved by its checksum at the time of checkout.

Simple branching
=================
Typical CVCS systems use cheap copy mechanisms when creating a new branch. Git branch management is very simple taking only a few seconds to create, delete, and merge branches.

Terminologies:
**************

Local Repository
================
VCS tool provide private workplace(s) for working copies. Prject contributors (developers) make changes/modifications within their private workplace then commit changes. These committed changes then become a part of the repository. Git takes it one step further by providing a private copy of the entire repository. Users can then perform multiple operations on the repository such as add file, remove file, rename file, move file, commit changes, etc... .

Working Directory vs. Staging Area (Index)
==========================================
The working directory is where files are checked-out. In other CVCS systems, developers typically make modifications and commit their changes directly to the repository. Git however doesn’t track every modified file. When users perform a commit operation, Git looks for the files present in the *staging area*. Only files within the staging area are candidates for commit.

Let's look at a basic Git workflow:

Step 1 : User1 modifies a file(s) within the working directory.

Step 2 : User1 then adds the modified file(s) to the staging area.

Step 3 : User1 performs a commit operation which moves the file(s) from the staging area. After a push operation, it persists the changes permanently to the Git repository.

.. figure:: https://s3.us-east-2.amazonaws.com/s3.nutanixtechsummit.com/git/image1.png

Suppose you modified two files, namely *foo.c* and *foobar.c* and you want two different commits for each operation. You can add one file in the staging area and do commit. After the first commit, repeat the same procedure for another file.

.. code-block:: bash

  # First commit
  [bash]$ git add foo.c

  # adds file to the staging area
  [bash]$ git commit –m “Added foo operation”

  # Second commit
  [bash]$ git add foobar.c

  # adds file to the staging area
  [bash]$ git commit –m “Added foobar operation”
  

Blobs
=====
Blob stands for Binary Large Object. File versions are represented by blob. Blobs contain file data (no metadata).  Git database, it's tagged as SHA1 hash of the file. 

Trees
=====
Tree's are objects that represent a directory containing blobs and sub-directories. Tree's are binary files that contain
references to blobs and trees which are also named as SHA1 hash of the tree object.

Commits
=======
A Commit maintains the current state of the repository and named by SHA1 hash. You might consider a commit-object as a node within a linked list, where each commit object has a pointer to the parent commit object. For a given commit, you can traverse back by looking at the parent pointer to view the history of a commit. If a commit has multiple parent commits, then that particular commit has been created by merging two branches.

Branches
========
Branches are used to create an alternate development stream. By default, Git maintains a master branch (a.k.a trunk). Branches are typically created to control workflow (i.e. a new feature or update). Once the feature or update is completed, it's merged with the master (trunk) branch. Every branch is referenced by HEAD, which points to the current commit within the branch. When commits are submitted, the HEAD pointer is updated to reflect the latest commit.

Tags
====
Tag's are used to assign meaningful names within a specific version of a repository. Tags are similar to branches, but are immutable - which implies a branch with no modification. Once a tag is created for a particular commit, even if you create a new commit, it will not be updated. Tags are typically used for product releases.

Clone
=====
Clones create a repository instance. Clone operations check-out working copies, as well as mirror the repository locally. Users can then perform multple operations on the local repository, followed by a pull (synchronizing distributed/cloned repositories over a network).

Pull
====
Pull operations copy changes from a remote repository instance to a local instance. The pull operation is used for synchronization between two repository instances.

Push
====
Push operations copy changes from a local repository instance to a remote instance, and is used to persist changes in a Git repository. 

HEAD
====
HEAD is a pointer, which points to the latest commit within a branch. Whenever you make a commit, HEAD is updated with the latest commit and are stored in **.git/refs/heads/** directory.

.. code-block:: bash
  
  [NTNX CentOS]$ ls .git/refs/heads/
  master

  [NTNX CentOS]$ cat .git/refs/heads/master
  2348387fded58fa4deadbeef6c21344ceda0289

Revision
========
Revisions represent the version of the source code. Revisions in Git are triggered by commits identified by SHA1 secure hashes.

URL
===
URLs represent the Git repository location. Git URLs are stored in the config file.

.. clode-block:: bash

  [NTNX CentOS foo_repo]$ pwd
  /home/foo/foo_repo

  [NTNX CentOS foo_repo]$ cat .git/config
  [core]
  repositoryformatversion = 1
  filemode = true
  bare = false
  logallrefupdates = true
  [remote "origin"]
  url = gituser@git.server.com:project.git
  fetch = +refs/heads/*:refs/remotes/origin/*
  
  
  
Install Git:
************

Create a CentOS Guest VM using the cluster's configured network.

Login to the CentOS Guest VM and use *yum* to install git as follows:

.. code-block:: bash

  [CentOS ~]$
   su -
   Password: *******

  [CentOS ~]# yum -y install git-core

  [CentOS ~]# git --version
  git version 1.7.1


Customize Git Environment:
**************************
Git provides the git config tool, which allows you to set configuration variables. Git stores all global configurations in *.gitconfig* file, which is located in the users home directory. To set these configuration values as global, add the *--global* option.  

**Note:** if you omit the *--global* option, then your configurations are specific for the current Git repository.

You can also set up system wide configuration. Git stores these values in the */etc/gitconfig* file, which contains the configuration for every user and repository on the system. To set these values, you must have *root* privledges and use the *--system* option.

When the above code is compiled and executed, it produces the following result:

Setting username
================
This information is used by Git commits.

.. code-block:: bash

  [booboo@CentOS project]$ git config --global user.name "booboo bear"
  
Setting email ID
================
This information is used by Git commits.

.. code-block:: bash

  [booboo@CentOS project]$ git config --global user.email "you@someemaildomain.com"

Avoid merge commits for pulling
===============================
You pull the latest changes from a remote repository, and if these changes are divergent, then by default Git creates merge commits. We can avoid this via following settings.

.. code-block:: bash

  [booboo@CentOS project]$ git config --global branch.autosetuprebase always
  

Color highlighting
==================
The following commands enable color highlighting for Git in the console.

.. code-block:: bash

  [booboo@CentOS project]$ git config --global color.ui true
  [booboo@CentOS project]$ git config --global color.status auto
  [booboo@CentOS project]$ git config --global color.branch auto


Setting default editor
======================
By default, Git uses the system default editor, which is taken from the VISUAL or EDITOR environment variable. We can configure a different one by using git config.

.. code-block:: bash

  [booboo@CentOS project]$ git config --global core.editor vim
  
Setting default merge tool
==========================
Git does not provide a default merge tool for integrating conflicting changes into your working tree. We can set default merge tool by enabling following settings.\\

.. code-block:: bash

  [booboo@CentOS project]$ git config --global merge.tool vimdiff
  
Listing Git settings
====================
To verify your Git settings of the local repository, use git config –list command as given below.

.. code-block:: bash

  [booboo@CentOS ~]$ git config --list
  user.name=booboo bear
  user.email=booboo@jellystone.com
  push.default=nothing
  branch.autosetuprebase=always
  color.ui=true
  color.status=auto
  color.branch=auto
  core.editor=vim
  merge.tool=vimdiff
 
