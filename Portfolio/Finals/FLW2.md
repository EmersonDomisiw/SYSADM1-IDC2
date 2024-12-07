+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 2a26569ee8434c4b93c98c31d50fc8bd |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: Domisiw, Emerson P.        | DATE PERFORMED:        |          |
|                                  | 11-21-24               |          |
+----------------------------------+------------------------+----------+
| Section: BSIT-IDC2               | DATE SUBMITTED:        |          |
|                                  | 11-21-24               |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Git Basics

Answer the following research questions about Git, GitLab desktop and
GitHub.

1.  What is Git, and why is it important in software development?

-   It is a DevOps tool that is used for resource code management. Git
    is a free and open-source version control system that handles small
    to very large projects efficiently. It also uses for tracking
    changes in the source code. It allows multiple developers to work
    together in software development.

2.  How does Git track changes in a project?

-   To track Git changes in a project, git add specifies what will go in
    a snapshot (putting the things in the working directory), and git
    commit will take the actual changes, once it is committed, it will
    make a permanent record of it.

3.  What is the difference between a local repository and a remote
    repository in Git?

-   The difference between a local repository and a remote repository in
    Git is that a local repository is hosted locally in a user's
    computer while the remote repository in the other hand is hosted
    remotely, maybe present anywhere and it is shared with several
    members of the team (It could be on the internet or same system on a
    different route).

4.  What are the basic Git commands?

-   **git init**: used to create an empty Git repository.

-   **git add**: used to add any new or modified files.

-   **git commit**: used to make sure that the changes you make are
    saved to the local directory.

-   **git status**: tells the current state of the repository.

-   **git config**: used to configure the user, name and user email.

-   **git log**: shows the order of the commit history for a repository.

-   **git pull**: used to fetch and merge changes from the remote to
    local repository.

-   **git clone**: used to create a local working copy of an existing
    remote repository.

5.  How do you check the status of a Git repository?

-   Use the command "git status", this will tell the current state of
    the repository. If the file you created are in the staging area but
    not have been committed, it will be shown by the git status.

6.  What is the purpose of branches in Git, and how do you create and
    switch between them?

-   Without interfering the source code, Git branches offer an organized
    way of managing code changes that allows the easy incorporation of
    new features, test concepts and fixing bugs. To switch between
    branches, "git checkout" command is used.

7.  What are GitLab Desktop and GitHub, and how are they different from
    Git?

-   Both GitLab Desktop and GitHub operate as a cloud service while a
    Git operates locally on the host device. GitLab sets itself apart as
    an integrated DevOps platform that offers CI/CD pipelines and ideal
    tool chain for the lifecycle of entire software development. GitHub
    caters to social coding and open-source communities.

8.  How do you connect a local Git repository to a GitLab or GitHub
    repository?

-   To connect a local Git repository to a GitLab or GitHub repository,
    we need first to create a repository on GitLab or GitHub, start a
    local Git repository if not done, then you need the remote using the
    command "git remote add origin \<repository url\>", and push your
    changes with the command "git push --u origin main".

9.  What are the steps to collaborate with others using GitLab or
    GitHub?

-   Steps:

> \- Create a repository on GitHub.
>
> \- Clone the repository to your local machine.
>
> \- Make changes you want and commit.
>
> \- Push your branch to the remote repository.
>
> \- Create a Pull Request (PR) or Merge Request (MR) on GitHub or
> GitLab.
>
> \- Review and discuss the changes with your team.
>
> \- Merge the PR/MR after approval.
>
> \- Pull the latest changes to stay updated with the main branch.

\- Resolve conflicts if needed.

10. How do you resolve merge conflicts in Git?

-   Use the command "git checkout \<branch\>" before you merge it.

-   Use the "git mergetool" to run one of the several merge to resolve
    the merge conflicts.

-   Reset the branch to the state before merging by using "git reset"
    command.

11. What is a pull request, and why is it used in GitHub?

-   It is a type of proposal to merge changes from one branch to
    another. It is used in GitHub for the reason that the collaborators
    can review the changes on the proposal before they combine the
    changes into a source code. It can also facilitate code reviews that
    maintains a well-documented codebase.

12. What are some best practices for writing commit messages?

-   Use the imperative mood

-   Separate subject and body

-   Keep the Subject Line Concise

-   Commit Related Changes

-   Write Good Commit Messages
