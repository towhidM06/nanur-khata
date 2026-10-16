# Nanu's Recipe Book

## Chapter 1: The First Recipe

I started by configuring my Git username and email. Then I created the nanur-khata folder and initialized a Git repository. I created bhapa-pitha.md and checked its status before staging it.

Nanu corrected the recipe because the original amount of gur was wrong. I used git diff to see the unstaged change and git diff --staged to inspect the staged version. This helped me understand the difference between the working directory and the staging area.

After correcting the recipe, I committed it with a meaningful message. I also created bazar-list.txt and accidentally staged it. I used git reset bazar-list.txt to unstage it without deleting the file.

**Figure 1 Git Setup**

![Figure 1 Git Setup](screenshots/Figure%201%20Git%20Setup.png)

**Figure 2 Stage Recipe**

![Figure 2 Stage Recipe](screenshots/Figure%202%20Stage%20Recipe.png)

**Figure 3 Check Differences**

![Figure 3 Check Differences](screenshots/Figure%203%20Check%20Differences.png)

**Figure 4 First Commit**

![Figure 4 First Commit](screenshots/Figure%204%20First%20Commit.png)

**Figure 5 Unstage File**

![Figure 5 Unstage File](screenshots/Figure%205%20Unstage%20File.png)

## Chapter 2: The Secret Spice

I created a private spice file, several temporary files and a draft folder. I did not want these files to become part of the repository. I added rules to .gitignore for the secret file, all .tmp files and the draft folder.

I used git status --short to check the repository and git check-ignore -v to confirm that the ignore rules applied. Finally, I committed only .gitignore. The secret spice blend remained on my computer and was not committed.

**Figure 6 Git Ignore**

![Figure 6 Git Ignore](screenshots/Figure%206%20Git%20Ignore.png)


## Chapter 3: The Eid Special

I created the eid-special branch to work on the Eid recipes separately. I added biryani.md and shemai.md in two separate commits. When I returned to main, these files were not present until I merged eid-special.

For the challenge, I changed the same biryani line differently on main and spice-experiment. Git could not automatically decide which version to keep, so it reported a merge conflict. I inspected the conflict markers, edited the file to create one final recipe, staged the resolved file and committed the merge resolution.

This exercise showed me that branches let me work independently, while merging combines changes. Conflicts need a decision when different branches modify the same part of a file.

**Figure 7 Create Eid Branch**

![Figure 7 Create Eid Branch](screenshots/Figure%207%20Create%20Eid%20Branch.png)

**Figure 8 Commit Eid Recipes**

![Figure 8 Commit Eid Recipes](screenshots/Figure%208%20Commit%20Eid%20Recipes.png)

**Figure 9 Merge Eid Branch**

![Figure 9 Merge Eid Branch](screenshots/Figure%209%20Merge%20Eid%20Branch.png)

**Figure 10 Merge Conflict**

![Figure 10 Merge Conflict](screenshots/Figure%2010%20Merge%20Conflict.png)

**Figure 11 Resolve Conflict**

![Figure 11 Resolve Conflict](screenshots/Figure%2011%20Resolve%20Conflict.png)

## Chapter 4: Mitu Joins In

I created a GitHub repository and connected my local repository using git remote add origin. I pushed my work to GitHub and cloned the repository into a second folder to act as Mitu.

Mitu added chittagong-mezban.md, committed the recipe and pushed it to the remote repository. I returned to my original folder and used git fetch origin to download the latest remote information. I then merged origin/main to integrate the changes.

When Mitu pushed another update, I used git pull origin main to update my local repository.

**Figure 12 GitHub Remote**

![Figure 12 GitHub Remote](screenshots/Figure%2012%20GitHub%20Remote.png)

**Figure 13 Add Mezban Recipe**

![Figure 13 Add Mezban Recipe](screenshots/Figure%2013%20Add%20Mezban%20Recipe.png)

### Fetch + Merge vs Pull

git fetch downloads remote changes and updates remote-tracking branches without automatically integrating them into my current branch. I can inspect the changes and merge them separately.

git pull fetches remote changes and integrates them into the current branch. Depending on the Git configuration, the integration may use a merge or rebase.

Using fetch and merge helped me understand each operation separately, while pull provided a convenient way to update the repository.


**Figure 14 Fetch and Merge**

![Figure 14 Fetch and Merge](screenshots/Figure%2014%20Fetch%20and%20Merge.png)

**Figure 15 Pull Updates**

![Figure 15 Pull Updates](screenshots/Figure%2015%20Pull%20Updates.png)

## Chapter 5: Half-Cooked Halua and Time Travel

I started writing the halua recipe and used git stash to save my unfinished work. I then corrected the biryani recipe by adding cardamom and committed the change. After that, I restored the halua work using git stash pop and completed the recipe.

I organized the recipes into a folder using git mv and removed an outdated recipe using git rm. I inspected the history using git log --stat -M and examined a particular commit using git show.

Finally, I created a separate reset-test branch, made two test commits and used git reset --hard to return to an older commit. I checked the history and saw that the test changes were no longer present on that branch.

**Figure 16 Stash Halua**

![Figure 16 Stash Halua](screenshots/Figure%2016%20Stash%20Halua.png)

**Figure 17 Restore Halua**

![Figure 17 Restore Halua](screenshots/Figure%2017%20Restore%20Halua.png)

**Figure 18 Move Recipe Files**

![Figure 18 Move Recipe Files](screenshots/Figure%2018%20Move%20Recipe%20Files.png)

**Figure 19 Remove Recipe**

![Figure 19 Remove Recipe](screenshots/Figure%2019%20Remove%20Recipe.png)

**Figure 20 Show Commit**

![Figure 20 Show Commit](screenshots/Figure%2020%20Show%20Commit.png)

**Figure 21 Reset Test Branch**

![Figure 21 Reset Test Branch](screenshots/Figure%2021%20Reset%20Test%20Branch.png)



### Why Rebase and Reset --hard Are Dangerous on Shared Branches

Rebase rewrites commit history by replaying commits with new commit IDs. This can confuse collaborators who are already using the original commits.

git reset --hard moves the current branch to an earlier commit and resets the staging area and working directory. Uncommitted changes can be lost, and commits removed from the branch may disappear from normal history.

These commands can disrupt shared work when other people depend on the existing history. I used a separate test branch for the reset demonstration and kept main intact.

### Final Submission

**Figure 22 Git History Graph**

![Figure 22 Git History Graph](screenshots/Figure%2022%20Git%20History%20Graph.png)