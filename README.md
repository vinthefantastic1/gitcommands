## Some Useful Git Commands

#### rename branch
	git branch -m master main
	
	// create a new branch on the remote named "main"
	git push -u origin main
	
	// delete the old branch
	git push origin --delete master
	
#### Push to only 1 of multiple remotes
	git push origin
	git push origin2
	
#### check configuration
	git config --list
#### help 
	git help config 

#### remove items from staging
	git reset
	
#### remove a single file
	git rm --cached $FILE
	
#### see log
	git log

#### show last commit
	git log -1

#### clone a repo

	git clone <url> <where to clone>
	git clone https://github.com/sdfsdfs sf sdfsf .  (dot means current directory)

#### view information
	git remote -view
	git branch -a

#### show changes
	git diff

#### to send to repository
	// origin = name of remote repository
	// main = branch of remote repository
	git pull origin main
	git push origin main

### Common Workflow:

    
#### Create a BRANCH  of desired feature that you're working on
	git branch my-new-feature
#### to start working on branch, check it out
	git checkout my-new-feature
#### after commiting to new repository
	git push -u origin my-new-feature
	git branch --show-current
	
### after UNIT tests worked fine. THEN MERGE

	git checkout main
	git pull origin main

	git branch --merged
	git merge my-new-feature
	git push origin main

#### AFTER you have merged your feature branch you can delete the branch

	git branch --merged
	git branch -d my-new-feature
	git branch -a 
	git push origin --delete my-new-feature

### ROLLBACK SOME BAD CHANGES
####  after you've made a bad commit..
	git status
	git diff

#### check it out again
	git checkout calc.py   (if not committed)

#### amend commit
	git commit --amend  (will bring up window)

	git log --stat (status of rep	)

#### MOVE feature to a different branch
	git cherry-pick

#### you want to remove a commit from the main branch
	git reset --soft  (hash of commit)
#### use this one most of the time
	git reset --mixed  hash of commit (default if not speciified)
	# then do a git checkout (filename)

	git reset hard  (makes all tracked files match. WILL GET RID of changes.  Untracked files are ok)

	git clean -df  (get rid of untracked files and directories)

	git reflog (shows what we've been doing) ... enables to find where missing files are

#### remove change if others have already downloaded code:
	git revert (with hashcode)






