# Git-Tutorial
Git Commands


1. Create Branch from the Current Project State
	- git branch <branch_name>
	- git checkout -b <branch_name>

2. Git Commit
	- git commit -m <message>

3. Get the Code of Perticular Commit
	- git checkout <commit_hash_string>

4. Merging the Code with Master Branch
	- git checkout master
	- git merge <other_branch>

5. Force Branch to have previous commit code
	- git branch -f <branch_name> HEAD~3
	- git branch -f <branch_name> HEAD^

6. Undo Commit Chnages in local and remote
	- git reset HEAD~1 (for local machine)(takes current branch 1 level back in commmit)
	- git revert HEAD~1 (for remote)(creates new commit with the specified previous commit code)

7. Merging with Git Rebase
	- Building Branch again with sequence of commits
	- git rebase -i HEAD~4

8. Include Other Multiple Commits Code in Current Branch
	- git cherry-pick <commit1> <commit2> ...
	- It Creates the extra comits eg. commit1', commit2'
	- You can work by Checking out perticular commit

9. Moving Back feature branch to master branch code
	- We created a feature branch for debug and print statements, after finding error go back to
	master branch again and fix error part only.
	- 

10. Giving Tag to Important Commits
	- git tag <tag_name> <commit>
	- eg. git tag v1 c3

11. Git Describe
	- Tells us about the specified branch how far it is from closest tag
	- git describe <branch_name>
	- its output like <closest_tag>_<no_of_commits_to_that_tag>_g<commit_hash>

	
-------------------------------------------------------------------------------------

REMOTE GIT

1. Git Clone
	- Clone the Remote Repo and Checkout to master branch
	
2. Git Fetch (Generally Used)
	- Get the Latest chnages from Remote Repository about new Commits or Branches Created
	- Run at Start of the Day
	
3. Git Pull (Mostly not Used)
	- Gets all Latest Code Branches and Commits and merge them with Local Code.
	
4. Git Push
	- Updates the Local Code Commits to Remote Repository.
	
5. Fixing Code Conflicts
	- You Pulled the Code, while doing chnages in a meanwhile someone else also pulled
	the code done the chnages, commits and pushed their code to remote repository. After this
	our git push commnad will be ambigious. So we have to merge our chnages with Latest Remote
	Repository Code and Solve the Conflicts then Push.
	- git fetch; git rebase origin/master; 
	- Then Check Code by Running, Resolve Issues
	- git push
	
6. Log All Commits
	- git log --stat
