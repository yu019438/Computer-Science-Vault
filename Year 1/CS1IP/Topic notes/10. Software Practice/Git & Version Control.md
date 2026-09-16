#CS1IP 
## Version control
Successfully writing a program can take several attempts, requirements/specification for the program can adapt/change over time, and many programmers may collaborate and share code at the same time
Ways you can solve this:
- Saving multiple files (e.g. `Task1.java`, `Task2.java` etc.)
- Share files through email, saving iterations of the source code
- Use a shared drive
However, the best way is to use 'Version control' through a system such as Git (most common)
## Git
- Git itself is the underlying version control system. Various services host git repositories remotely.  GitHub is the best known but GitLab is another (open-source).
- A repository stores all versions of a project's source code. Usually there's a repository on a server, called the **remote** a programmer can copy it to their own device:
-  `git clone REMOTE-REPOSITORY`
- Then the files can be edited locally, before being 'pushed' back to the repo
### Git commands
- `Git diff`: Allows the user to see local changes made against repo files
- `Git add`: Stages selected files/changes and marks them as ready to be included in the next commit (does not save/push anything yet) 
- `Git commit`: *(followed by a message describing the changes)*: Saves staged changes to the **local** repository as a permanent snapshot 
- `Git push`: Sends committed changes from the local repository to the remote repository
- `Git pull`: Gets the latest version of files from the remote repository 
- `Git merge`: Combines changes from two different sources (e.g. local branch and the remote). Happens automatically as part of `git pull` if you and another programmer collaborated/changed different parts of a file (can cause merge conflict that must be solved manually)
---
## Covered in
- [[CS1IP_week_02_lecture.pdf]]
