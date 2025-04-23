# Git Cheat Sheet

## Initial Configuration
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Create & Clone Repository
```bash
git init                    # Initialize new repository
git clone <repo-url>        # Clone existing repository
```

## Staging & Committing
```bash
git status                   		# Show working directory status
git add <file>               		# Stage specific file
git add .                    		# Stage all changes
git commit -m "message"      		# Commit staged changes
git cherry-pick <commit_id>  		# Copy a commit of one branch to another
git reset --soft HEAD^		 		# Uncommit a local commit and stage all changes
git push --force origin <branch>	# Force a push if this is blocked
git --allow-empty -m "message"		# Launch an empty commit
```

## Viewing History
```bash
git log                    	# Show commit history
git log --oneline          	# Condensed commit log
git show <commit_id>		# Show the content of a commit
```

## Branching
```bash
git branch                 # List branches
git branch <branch>        # Create new branch
git checkout <branch>      # Switch to branch
git switch <branch>        # Modern alternative to checkout
git merge <branch>         # Merge branch into current
```

## Remote Repositories
```bash
git remote add origin <url>     			# Add remote repository
git push -u origin main         			# Push to remote (initial)
git push                        			# Push changes
git pull                        			# Pull latest changes
git pull --rebase=false origin <branch>		# Disable a rebase instruction in a pull process
git diff > <patch_name>.patch 				# Create a patch to move local changes to another repository
```

## Undoing Changes
```bash
git checkout -- <file>          			# Discard local changes
git reset HEAD <file>           			# Unstage file
git restore <file>           				# Restore file
git revert <commit_id>          			# Revert a specific commit
git reset --soft HEAD~						# Undo the last local commit
git reset --hard HEAD~<number_of_commits>	# Remove the last local commits
```

## Squashing
```bash
git reset --soft HEAD~<number_of_commits> &&
git commit 										# Combines multiple commits into one. Use both lines
```

## Delete Local Branches
```bash
git branch -D <branch>          # Delete local branch
```

## Ignoring Files
Use a `.gitignore` file:
```
*.log
*.tmp
node_modules/
```
