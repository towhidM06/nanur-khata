# Nanu's Recipe Book

## Chapter 1: The First Recipe

I started by configuring my Git username and email. Then I created the nanur-khata folder and initialized a Git repository. I created bhapa-pitha.md and checked its status before staging it.

Nanu corrected the recipe because the original amount of gur was wrong. I used git diff to see the unstaged change and git diff --staged to inspect the staged version. This helped me understand the difference between the working directory and the staging area.

After correcting the recipe, I committed it with a meaningful message. I also created bazar-list.txt and accidentally staged it. I used git reset bazar-list.txt to unstage it without deleting the file.


## Chapter 2: The Secret Spice

I created a private spice file, several temporary files and a draft folder. I did not want these files to become part of the repository. I added rules to .gitignore for the secret file, all .tmp files and the draft folder.

I used git status --short to check the repository and git check-ignore -v to confirm that the ignore rules applied. Finally, I committed only .gitignore. The secret spice blend remained on my computer and was not committed.

## Chapter 3: The Eid Special

I created the eid-special branch to work on the Eid recipes separately. I added biryani.md and shemai.md in two separate commits. When I returned to main, these files were not present until I merged eid-special.

For the challenge, I changed the same biryani line differently on main and spice-experiment. Git could not automatically decide which version to keep, so it reported a merge conflict. I inspected the conflict markers, edited the file to create one final recipe, staged the resolved file and committed the merge resolution.

This exercise showed me that branches let me work independently, while merging combines changes. Conflicts need a decision when different branches modify the same part of a file.

## Chapter 4: Mitu Joins In

I created a GitHub repository and connected my local repository using git remote add origin. I pushed my work to GitHub and cloned the repository into a second folder to act as Mitu.

Mitu added chittagong-mezban.md, committed the recipe and pushed it to the remote repository. I returned to my original folder and used git fetch origin to download the latest remote information. I then merged origin/main to integrate the changes.

When Mitu pushed another update, I used git pull origin main to update my local repository.

### Fetch + Merge vs Pull

git fetch downloads remote changes and updates remote-tracking branches without automatically integrating them into my current branch. I can inspect the changes and merge them separately.

git pull fetches remote changes and integrates them into the current branch. Depending on the Git configuration, the integration may use a merge or rebase.

Using fetch and merge helped me understand each operation separately, while pull provided a convenient way to update the repository.