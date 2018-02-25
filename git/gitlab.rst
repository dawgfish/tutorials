*************
Lab - Git
*************


Introduction:
*************
Git is a distributed revision control and source code management system with an emphasis on speed. Git was initially designed and developed by Linus Torvalds for Linux kernel development and is a free software distributed under the terms of the GNU General Public License.

This lab guides users how to use Git for project version control in a distributed environment while working on source code and non-source code projects.

The Lab will help beginners learn the basic functionality of Git version control system. After completing this lab, participants will have a moderate level of expertise in using Git version control system to build upon.

This lab assumes participants are going to use Git to handle various projects. It's good to have some exposure to software development life cycle and working knowledge of application development but not required.


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

Fast and Compact:
=================
Most of the operations are performed locally providing benefit in terms of speed. Git doesn't depend on a central server; which is why there's no need to interact with remote server(s) for every operation. Git's core is written in C, which avoids runtime overhead associated with other high-level (interpreted) languages. Git mirrors an entire repository, the size of the data on the client side is small, illustrating the efficiency of Git at compressing and storing data on the client side.

Implicit backup:
================
The chances of losing data are reduced because there are multiple distributed copies. Data present on any client mirrors the repository so it can be used in the event of data corruption or disk crash

Security:
=========
Git uses a widely adopted cryptographic hash function called secure hash function (SHA1), to name and index objects within its database. Every file and commit is check-summed and retrieved by its checksum at the time of checkout.

Simple branching:
=================
Typical CVCS systems use cheap copy mechanisms when creating a new branch. Git branch management is very simple taking only a few seconds to create, delete, and merge branches.

Terminologies:
**************


