# Nanu's Recipe Book

## Chapter 1: The First Recipe

I started by configuring my Git username and email. Then I created the nanur-khata folder and initialized a Git repository. I created bhapa-pitha.md and checked its status before staging it.

Nanu corrected the recipe because the original amount of gur was wrong. I used git diff to see the unstaged change and git diff --staged to inspect the staged version. This helped me understand the difference between the working directory and the staging area.

After correcting the recipe, I committed it with a meaningful message. I also created bazar-list.txt and accidentally staged it. I used git reset bazar-list.txt to unstage it without deleting the file.
