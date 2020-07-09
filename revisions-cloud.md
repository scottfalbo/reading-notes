# Revisions and the Cloud

#### VCS

> **Version Control System (VCS)** is a system that allows to revisist previous instances of a file and groups of files.  This is useful for reverting files to previous states, tracking modifcation and comparing changes.
>> + *Local Version Control*: A database on your hard disk that stores changed files.
>> + *Centralized Version Control (CVCS)*: A single server that stores all changes and file version that can be accessed by multiple clients.  This is crucial in collaborative work as team members can see and track what others are doing and leaders have more control over the scope.
>> + *Distributed Version Control (DVCS)*: Building on CVCS distributed version control allows clients to create mirrored repositories that act as data backups to replace any lost information in the event of hardware issues or corruption.

#### Git

> Git is a DVCS that stores data in a file system made up of **snapshots**.  Each time you **save (commit)** a change Git creates a snapshot and stores a reference to it.  Git uses mostly **local operations** because most project information can be found in local storage.  This eliminates the need to fetch data and allows for offline work.  Every **change** made to any file or directory is **tracked** by Git.  Git will always detect corrupted files or loss of information in trasnfer.  By tracking changes and taking snapshots Git greatly reduceds the possibility of **data loss.**  Files in Git can reside in three main states:
>> + **Committed**: Data is securely stored in a local database.
>> + **Modified**: File has been changed but not committed to the database
>> + **Staged**: Flagged a file's changed version to be committed in the next snapshot.

[Git Documentation](https://git-scm.com/doc)

**GitHub** is the physical location, or server, where the files are stored.

**Local vs Remote**: Local refers to files stored locally on your hard disk.  Remote files are stored on another server and accessed by the client.

**Clone**: A clone is an exact copy of your Git repository.

**ACP** Add, Commit, Push.  This is the process used to create a snapshot of you project.
+ Add: `git add file`
+ Commit: `git commit -m "meaningful notation, why are you saving"
+ Push: `git push origin master` 

**Deployment** is the launching of your files to a live site.

<br>

[Back to the mainpage](README.md)<br />
[Growth Mindset](growth-mindset.md)<br />
[Markdown Notes](markdown-notes.md)<br />
[Coder's Computer](coders-computer.md)




