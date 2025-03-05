# advancedGitHubExercises

Part 1:

1. Missing File Fix
    git add test4.md
    git commit --amend -m "chore: Create third and fourth files"


2. Editing Commit History
    git rebase -i HEAD~2
    changing pick to reword
    commiting: "Crea second file"

3. Editing Commit History
    git rebase -i HEAD~2
    changing pick to squash
    commiting: "Crea second file"

4. Editing Commit History
    git reset HEAD~1 : to go back to previous commit
    git add test3.md
    git commit -m "chore: Create third file"
    git add test4.md
    git commit -m "chore: Create fourth file"

5. Advanced Squashing
    git rebase -i HEAD~2
    Changing pick to squash

6. Dropping a Commit
    touch unwanted.txt
    git add unwanted.txt
    git commit -m "Unwanted commit"
    git rebase -i HEAD~1
    changing pick to drop

7. Reordering Commits
    git rebase -i HEAD~3
    Reorder the commits as needed.

8. Cherry-Picking Commits
    git checkout -b ft/branch
    touch test5.md
    git add test5.md
    git commit -m "Implemented test 5"
    git checkout main
    git cherry-pick <commit-hash>

Part 2: Branching Basics
1. Create a Feature Branch
    git checkout -b ft/new-feature
    
2. Work on the Feature Branch
    echo "Feature content" > feature.txt
    git add feature.txt
    git commit -m "Implemented core functionality for new feature"

3. Switching Back and Adding More Changes
    git checkout main
    echo "Project README" > readme.txt
    git add readme.txt
    git commit -m "Updated project readme"

4. Pushing Branches
    git push origin ft/new-feature

5. Deleting a Branch
    git branch -d ft/new-feature

6. Create a Branch from a Commit
    git checkout -b ft/new-branch-from-commit <commit-hash>

7. Merging a Branch
    git checkout main
    git merge ft/new-branch-from-commit

8. Rebasing a Branch
    git checkout ft/new-branch-from-commit
    git rebase main

9. Renaming a Branch
    git branch -m ft/new-branch-from-commit ft/improved-branch-name

10. Detached HEAD
    git checkout <commit-hash>
    To retutn: git checkout main


Part 3:

1. Stashing Changes
    git stash
2. Retrieving Stashed Changes
    git stash pop
3. Simulating Merge Conflict
    Modify a file in both main and ft/feature-branch.
    Merge the branches:
    git checkout main
    git merge -m ft/feature-branch

5. .gitignore File
    echo "/tmp" > .gitignore
    git add .gitignore
    git commit -m "chore: Ignore tmp files"
   
9. Pushing to Remote
    git push origin main
   
11. Pulling from Remote
    Modify README.md on GitHub.
    Then Pull changes:
        git pull origin main
