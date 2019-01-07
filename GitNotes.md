#Create New Branch
git checkout -b [yourBranchName]-#<issueNumber>

#Save Changes
git add .
git commit -m "[message]"

##If not merging directly in VS.Code
git push origin [yourBranchName]-#<issueNumber>

#OPTION TO MERGE DIRECTLY IN V.S.CODE (USE IF RESOLVING CONFLICTS LOCALLY)
<!-- resolve all conflicts directly in this file. Otherwise the conflicts will have to be resolved AFTER the pull request is made -->

    ##Update YOUR Master Branch
git checkout master
git pull
git checkout [yourBranchName]-#<issueNumber>
git merge master

    ##Push your code
git push
<!-- If you get "fatal: The current branch footer has no upstream branch." Use:--> 
git push --set-upstream origin [yourBranchName]-#<issueNumber>
<!-- See video here for more: https://youtu.be/oFYyTZwMyAg  -->

#On GitHub
-Go to pull requests. 
-Click the green button "New Pull Request".
-Select [yourBranchName]-#<issueNumber> from the compare drop-down. 
-You should see a green check-box and "Able to merge. These branches can be automatically merged."
-Click "Create pull request" (green button)

#Deleting your local branch (Once merged)
git branch -D [yourBranchName]-#<issueNumber>

#Deleting the branch on git (Once merged)
git push origin --delete [yourBranchName]-#<issueNumber>
<!-- alternatively you can delete your branch by clicking the trash can by your branch after clicking the branches option from the repository on git-hub. -->