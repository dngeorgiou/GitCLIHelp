# Common Git commands:

// Check status  
$ git status

// Add a new remote  
$ git remote add {remoteName} {https://github.com/.../.git}

// See open remotes  
$ git remote -v

// Add file to be committed  
$ git add {fileName}

// Commit added files  
$ git commit -m "message"

// Pull remote branch to local repository  
$ git pull {remoteName} {branchName}

// Push local branch to remote repository  
$ git push {remoteName} {branchName}

// Remove file from repository and file system  
$ git rm {fileName}

// Remove file from just repository  
$ git rm --cached {fileName}


# Differences in files
// Show differences between index and working tree,  
// that is, changes you haven't staged to commit  
$ git diff {filename}

// Show differences between current commit and index,  
// that is, what you're about to commit  
// --staged does exactly the same thing, use what you like  
$ git diff --cached {filename}

// Show differences between current commit and working tree  
$ git diff HEAD {filename}


# Revert to old commit/state
// This will detach your HEAD, that is, leave you with no branch checked out  
$ git checkout {first 9 #'s of git commit}

// Make new branch at old commit and go there  
$ git checkout -b old-state {first 9 #'s of git commit}

// Revert working copy to most recent commit  
$ git reset --hard HEAD

// Revert working copy to {#} commits previous  
$ git reset --hard HEAD^{#}


# Branching
// Create and move to {branchName}  
$ git checkout -b {branchName}

// Move to {branchName}  
$ git checkout {branchName}

// Delete merged local branch  
$ git branch -d {branchName}

// Delete not-merged local branch  
$ git branch -D {branchName}

// Delete {branchName} from {remoteName}  
$ git push --delete {remoteName} {branchName}

// Merge {branchName} with branch currently on  
$ git merge {branchName}


# Create new repository on the command line
$ echo "# {repository_name}" >> README.md  
$ git init  
$ git add README.md  
$ git commit -m "first commit"  
$ git remote add origin https://github.com/{account_name}/{repository_name}  
$ git push -u origin master  


# Push an existing repository from the command line
$ git remote add origin https://github.com/{account_name}/GitCLIHelp.git  
$ git push -u origin master  