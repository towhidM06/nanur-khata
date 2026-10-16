# Nanu's Recipe Book

## Chapter 1: The First Recipe

I started by configuring my Git username and email. Then I created the nanur-khata folder and initialized a Git repository. I created bhapa-pitha.md and checked its status before staging it.

Nanu corrected the recipe because the original amount of gur was wrong. I used git diff to see the unstaged change and git diff --staged to inspect the staged version. This helped me understand the difference between the working directory and the staging area.

After correcting the recipe, I committed it with a meaningful message. I also created bazar-list.txt and accidentally staged it. I used git reset bazar-list.txt to unstage it without deleting the file.


## Chapter 2: The Secret Spice

I created a private spice file, several temporary files and a draft folder. I did not want these files to become part of the repository. I added rules to .gitignore for the secret file, all .tmp files and the draft folder.

I used git status --short to check the repository and git check-ignore -v to confirm that the ignore rules applied. Finally, I committed only .gitignore. The secret spice blend remained on my computer and was not committed.