## Research Questions 

Now that you are all set up, it's time to learn a little more about the tools of the trade. Edit this file and answer the following questions. You are going to need to start familiarizing yourself with the [GitHub docs](https://docs.github.com/en). Docs (short for documentation) are the instructions on how to use a languge or program. A large part of your job as a developer will be learning how to read and work with documentation. Please reference the GitHub docs when answering the questions below. If you cannot find what you are looking for in the docs, you can always start to practice your Google skills!

1. What is Git?
    Git is "a free and open source distributed version control system." It allows multiple contributors to work on a coding project simultaneously, keeping track of a history of changes and allowing for branches to be split and merged as needed to evolve the master repo.
2. What is the difference between Git and GitHub?
    Git is the program/system itself, the series of commands that allows for Git to do what it does. GitHub is an interface to allow for repository storage and for communal access.
3. Why do we create a branch?
    To allow us to work on a new feature/aspect without altering the original.
4. What is the purpose of a Pull Request?
    To submit for review changes made in the local repository that you would like merged with the remote repository.
5. What is the command you can use to switch between branches? For example you are working on the FIRSTNAME-LASTNAME branch and you want to switch back to main.
    'git branches' will list the branches available in the local repository, and 'git checkout <branch name>' will switch to the chosen branch.
6. Explain the difference between `git fetch`, `git merge` and `git pull`. What does each command do?
    'git fetch' accesses the remote repository and brings any changes to the local computer.
    'git merge' merges those changes to the local repository.
    'git pull' is essentially a two-for-one (fetch + merge) -- though less secure since comparison of differences by the user occurs after the fact (if at all). 
7. What is a merge conflict?
    git is adept at determining how to merge changes that are being made simultaneously. However, in certain instances, git will refuse to proceed with a merge:
    a) If the local repository is not up to date (Error message: "error: Entry '<fileName>' not uptodate. Cannot merge.").
    b) If there is a conflict between your submission and another developer's code (Error message: "error: Entry '<fileName>' would be overwritten by merge. Cannot merge.")
        i) If another developer attempts to edit the same lines of code that you have edited.
        ii) If the file you were working on is deleted from the remote repository.
8. How do you resolve a merge conflict?
    a) Resolve all conflicts with pending local changes (see: git stash, git checkout, git commit, git reset).
    b) Get in touch with the other developer to figure out what the issue is and how best to resolve it.
    *) Generally:
        i) 'git status' will give some indication as to what the merge conflict is.
        ii) 'cat merge.txt' will then output more specific information.
        iii) 'git log --merge' will list conflicting commits.
        iv) 'git merge --abort' will revert the branch to the pre-merge state
        v) 'git reset' will revert files to a previous known-to-be-functional state
        vi) 'git diff' will show differences between states of a repository/files, allowing for analysis. 
