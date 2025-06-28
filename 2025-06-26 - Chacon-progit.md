---
kindle-sync:
  bookId: "6807"
  title: progit
  author: Scott Chacon
  highlightsCount: 31
tags:
  - Dev-Ops
  - Version-Control
  - Git
  - Books
---
# progit
## Metadata
* Author: Scott Chacon

## Highlights
This makes Git more like a mini filesystem with some incredibly powerful tools built on top of it, rather than simply a VCS. — location: [456]() ^ref-25527

---
Git thinks about its data more like a stream of snapshots. Figure 5. Storing data as snapshots of the project over time This is an important distinction between Git and nearly all other VCSs. It makes Git reconsider almost every aspect of version control that most other systems copied from the previous generation. This makes Git more like a mini filesystem with some incredibly powerful tools built on top of it, rather than simply a VCS. — location: [452]() ^ref-54536

---
Git Has Integrity Everything in Git is checksummed before it is stored and is then referred to by that checksum. This means it’s impossible to change the contents of any file or directory without Git knowing about it. This functionality is built into Git at the lowest levels and is integral to its philosophy. You can’t lose information in transit or get file corruption without Git being able to detect it. The mechanism that Git uses for this checksumming is called a SHA-1 hash. This is a 40-character string composed of hexadecimal characters (0–9 and a–f) and calculated based on the contents of a file or directory structure in Git. — location: [472]() ^ref-59978

---
Modified means that you have changed the file but have not committed it to your database yet. ​▪​ Staged means that you have marked a modified file in its current version to go into your next commit snapshot. — location: [489]() ^ref-60981

---
Committed means that the data is safely stored in your local database. — location: [490]() ^ref-6884

---
The working tree is a single checkout of one version of the project. These files are pulled out of the compressed database in the Git directory and placed on disk for you to use or modify. — location: [493]() ^ref-11909

---
The staging area is a file, generally contained in your Git directory, that stores information about what will go into your next commit. Its technical name in Git parlance is the “index”, but the phrase “staging area” works just as well. The Git directory is where Git stores the metadata and object database for your project. This is the most important part of Git, and it is what is copied when you clone a repository from another computer. — location: [494]() ^ref-13507

---
The basic Git workflow goes something like this: You modify files in your working tree. You selectively stage just those changes you want to be part of your next commit, which adds only those changes to the staging area. You do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git directory. — location: [498]() ^ref-9033

---
If a particular version of a file is in the Git directory, it’s considered committed. If it has been modified and was added to the staging area, it is staged. And if it was changed since it was checked out but has not been staged, it is modified. — location: [501]() ^ref-2311

Git restore --staged restores files in staging area only

---
​ In the simple case, a repository might have a single .gitignore file in its root directory, which applies recursively to the entire repository. However, it is also possible to have additional .gitignore files in subdirectories. The rules in these nested .gitignore files apply only to the files under the directory where they are located. The Linux kernel source repository has 206 .gitignore files. — location: [840]() ^ref-54640

---
In the simple case, a repository might have a single .gitignore file in its root directory, which applies recursively to the entire repository. However, it is also possible to have additional .gitignore files in subdirectories. The rules in these nested .gitignore files apply only to the files under the directory where they are located. The Linux kernel source repository has 206 .gitignore files. — location: [841]() ^ref-44129

---
As an example, if you commit and then realize you forgot to stage the changes in a file you wanted to add to this commit, you can do something like this: $ git commit -m 'Initial commit' ^ref-32391
$ git add forgotten_file
$ git commit --amend You end up with a single commit — the second commit replaces the results of the first. — location: [1154]()

---
(use "git add <file>..." to update what will be committed) — location: [1225]() ^ref-47749

---
After your super-important fix is deployed, you’re ready to switch back to the work you were doing before you were interrupted. However, first you’ll delete the hotfix branch, because you no longer need it — the master branch points at the same place. You can delete it with the -d option to git branch: $ git branch -d hotfix ^ref-22627
Deleted branch hotfix (3a0874c). — location: [1655]()

---
They have another parallel branch named develop or next that they work from or use to test stability — it isn’t necessarily always stable, but whenever it gets to a stable state, it can be merged into master. It’s used to pull in topic branches (short-lived branches, like your earlier iss53 branch) when they’re ready, to make sure they pass all the tests and don’t introduce bugs. In reality, we’re talking about pointers moving up the line of commits you’re making. The stable branches are farther down the line in your commit history, and the bleeding-edge branches are farther up the history. — location: [1819]() ^ref-9028

---
Generally it’s better to simply use the fetch and merge commands explicitly as the magic of git pull can often be confusing. — location: [1991]() ^ref-62547

---
Figure 35. Simple divergent history The easiest way to integrate the branches, as we’ve already covered, is the merge command. It performs a three-way merge between the two latest branch snapshots (C3 and C4) and the most recent common ancestor of the two (C2), creating a new snapshot (and commit). — location: [2007]() ^ref-41410

---
Figure 36. Merging to integrate diverged work history However, there is another way: you can take the patch of the change that was introduced in C4 and reapply it on top of C3. In Git, this is called rebasing. With the rebase command, you can take all the changes that were committed on one branch and replay them on a different branch. — location: [2011]() ^ref-45661

---
Figure 38. Fast-forwarding the master branch Now, the snapshot pointed to by C4' is exactly the same as the one that was pointed to by C5 in the merge example. There is no difference in the end product of the integration, but rebasing makes for a cleaner history. If you examine the log of a rebased branch, it looks like a linear history: it appears that all the work happened in series, even when it originally happened in parallel. Often, you’ll do this to make sure your commits apply cleanly on a remote branch — perhaps in a project to which you’re trying to contribute but that you don’t maintain. In this case, you’d do your work in a branch and then rebase your work onto origin/master when you were ready to submit your patches to the main project. — location: [2026]() ^ref-55942

---
Note that the snapshot pointed to by the final commit you end up with, whether it’s the last of the rebased commits for a rebase or the final merge commit after a merge, is the same snapshot — it’s only the history that is different. Rebasing replays changes from one line of work onto another in the order they were introduced, whereas merging takes the endpoints and merges them together. — location: [2034]() ^ref-21877

---
Do not rebase commits that exist outside your repository and that people may have based work on. — location: [2078]() ^ref-38368

---
One point of view on this is that your repository’s commit history is a record of what actually happened. It’s a historical document, valuable in its own right, and shouldn’t be tampered with. From this angle, changing the commit history is almost blasphemous; you’re lying about what actually transpired. So what if there was a messy series of merge commits? That’s how it happened, and the repository should preserve that for posterity. The opposing point of view is that the commit history is the story of how your project was made. You wouldn’t publish the first draft of a book, so why show your messy work? When you’re working on a project, you may need a record of all your missteps and dead-end paths, but when it’s time to show your work to the world, you may want to tell a more coherent story of how to get from A to B. People in this camp use tools like rebase and filter-branch to rewrite their commits before they’re merged into the mainline branch. They use tools like rebase and filter-branch, to tell the story in the way that’s best for future readers. — location: [2131]() ^ref-52703

---
you to decide which one is best for your particular — location: [2142]() ^ref-61180

---
You can get the best of both worlds: rebase local changes before pushing to clean up your work, but never rebase anything that you’ve pushed somewhere. — location: [2142]() ^ref-1127

---
Git is smart enough to figure out what commit you’re referring to if you provide the first few characters of the SHA-1 hash, as long as that partial hash is at least four characters long and unambiguous; that is, no other object in the object database can have a hash that begins with the same prefix. — location: [4061]() ^ref-49854

---
Git can figure out a short, unique abbreviation for your SHA-1 values. If you pass --abbrev-commit to the git log command, the output will use shorter values but keep them unique; it defaults to using seven characters but makes them longer if necessary to keep the SHA-1 unambiguous: $ git log --abbrev-commit --pretty=oneline ^ref-61539
ca82a6d Change the version number
085bb3b Remove unnecessary test code
a11bef0 Initial commit — location: [4075]()

---
Finally, you may not want to stash some work or files in your working directory, but simply get rid of them; that’s what the git clean command is for. Some common reasons for cleaning your working directory might be to remove cruft that has been generated by merges or external tools or to remove build artifacts in order to run a clean build. You’ll want to be pretty careful with this command, since it’s designed to remove files from your working directory that are not tracked. If you change your mind, there is often no retrieving the content of those files. A safer option is to run git stash --all to remove everything but save it in a stash. — location: [4418]() ^ref-25470

---
If you ever want to see what it would do, you can run the command with the --dry-run (or -n) option, which means “do a dry run and tell me what you would have removed”. $ git clean -d -n ^ref-53134
Would remove test.o
Would remove tmp/ — location: [4427]()

---
The HEAD HEAD is the pointer to the current branch reference, which is in turn a pointer to the last commit made on that branch. That means HEAD will be the parent of the next commit that is created. It’s generally simplest to think of HEAD as the snapshot of your last commit on that branch. — location: [4799]() ^ref-53082

---
The Index The index is your proposed next commit. We’ve also been referring to this concept as Git’s “Staging Area” as this is what Git looks at when you run git commit. — location: [4809]() ^ref-3182

---
It’s important to note that this flag (--hard) is the only way to make the reset command dangerous, and one of the very few cases where Git will actually destroy data. Any other invocation of reset can be pretty easily undone, but the --hard option cannot, since it forcibly overwrites files in the working directory. In this particular case, we still have the v3 version of our file in a commit in our Git DB, and we could get it back by looking at our reflog, but if we had not committed it, Git still would have overwritten the file and it would be unrecoverable. Recap The reset command overwrites these three trees in a specific order, stopping when you tell it to: Move the branch HEAD points to (stop here if --soft). Make the index look like HEAD (stop here unless --hard). Make the working directory look like the index. — location: [4889]() ^ref-2658

---