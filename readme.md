# Git Branching Workflow – Mini Project
## Introduction

In real-world software development, multiple developers work on the same project simultaneously. If everyone directly modifies the main branch (main), it can easily break the stable version of the project. To solve this, developers use Git branching, which allows creating independent lines of development called branches.

![](images/versions)


## Branches help to:

Work on new features or bug fixes safely without affecting the main code

Experiment with changes without risking production code

Merge changes back into the main branch once they are tested and ready

In this mini project, we will create multiple branches (about_us, contact_us, home), make changes in each branch, merge them into the main branch, and push the final code to GitHub. This workflow is very common in DevOps and collaborative development.


## 🔹 Step 1: Check remote repository

First, check which remote repository is connected to the project. This ensures we can push our changes to GitHub later.

```bash
git remote -v
```

Next: Now that the remote is confirmed, we can start tracking changes in our local project by checking the status.

##  🔹 Step 2: Check status

Check which files are new, modified, or staged. This helps us understand what changes exist in the working directory.
```bash
git status -s
```


Next: We see that index.html is untracked. So, we need to add it to the staging area before committing.

##  🔹 Step 3: Add index.html and commit

Stage the file to be committed and then commit it to the repository.

```bash
git add .

git commit -m "added index.html file"
```


Next: Now that the main file is committed, we can start creating a new branch to work on a feature (about_us).

##  🔹 Step 4: Create a new branch about_us and switch to it

Create a new branch and switch to it for isolated feature development.
```bash
git branch about_us
git switch about_us
```


Next: We are now in the about_us branch. We will create a new page about.html and modify index.html.

##  🔹 Step 5: Add about.html, modify index.html, and commit

Make changes in this branch, stage them, and commit.
```bash
git add .
git commit -m "index and about is committed on about_us branch"
```


Next: The about_us feature is complete. We will now merge it into the main branch to include it in the main codebase.

##  🔹 Step 6: Switch to main branch and merge about_us

Return to the main branch and merge the about_us branch.
```bash
git checkout main
git merge about_us
```

Next: The main branch now has the about_us changes. We can continue by creating a new branch for the contact page.

##  🔹 Step 7: Create branch contact_us, add contact.html, modify index.html, and commit

Create a new branch for the contact page feature, add a new file, and commit changes.
```bash
git checkout -b contact_us
git add .
git commit -m "created contact.html and modified index.html"
```


Next: The contact_us feature is ready. We will create another branch for the home page feature.

##  🔹 Step 8: Create branch home, add home.html, and commit

Create a branch for the home page and commit the new file.
```bash
git checkout -b home
git add .
git commit -m "committed home page"
```

Next: All features are developed in separate branches. Now we will merge all feature branches into the main branch.

##  🔹 Step 9: Switch back to main and merge all feature branches

Switch back to the main branch and merge both contact_us and home branches.
```bash
git switch main
git merge contact_us
git merge home
```


Next: The main branch now contains all the features. Finally, we will push the updated main branch to GitHub.

##  🔹 Step 10: Final commit and push to GitHub

Stage any pending changes, commit them, and push everything to the remote repository.
```bash
git add .
git commit -m "all codes committed"
git push origin main
```

Next: All files and features are now pushed to GitHub. The project is ready for collaboration or further development.

##  ✅ Outcome:

Created multiple feature branches (about_us, contact_us, home)

Committed changes separately in each branch

Merged all branches into main

Pushed the final project to GitHub

