# Fix a Merge Conflict
1. Make sure you're in your repository directory.
2. Pull the most recent version of the repository from Bitbucket.

	`$ git pull`

3. Checkout the source branch.	

	`$ git checkout <feature_branch>`
	
4. Pull the destination branch into the source branch.

	`$ git pull origin <destination_branch>`

5. Resolve the conflic
6. Add and commit the change.
	
	`$ git add <filename>` 
	
	`$ git commit -m 'commit message'`

7. Push the change to the remote.
	
	`$ git push origin <feature_branch>`

8. When you check the pull request, the pull request will still be open and you'll no longer see any merge conflicts.