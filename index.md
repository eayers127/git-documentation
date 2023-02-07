Git Basics:
1. What is Git?
Git is a version control system. It keeps your drafts organized.
Git is a distributed control system, meaning that everyone has their own copy of the repo on their machine.

2. Why use Git? What problem does it solve?
Git allows for multiple developers to be in the same file making changes.
Git makes branching and merging easier. 
Git is secure.

3. What is the difference between Git and Github?
Github uses Git. Github is a repository service. It hosts repositories.
There are other hosting services like BitBucket that are similar services as Github.

Git Rebase:
1. What is Git rebase?
Rebase changes the base commit of the merge. It rewrites history and is destructive.

2. What are some advantages and disadvantages of Git rebase?
Rebase allows changes to be added from one branch to another. The history is cleaner and becomes linear.
Rebase is destructive, so you could lose work. You cannot track the history as well. Rebase does not work with pull requests.

3. When shouldn't you use Git rebase? Why?
It is dangerous to lose commits and it rewrites history. It should not be used when working on the same project as another developer because it messes with the history.
Do not use it on public projects because other developers are still on the original main branch.

Rebase merge:
![image](https://user-images.githubusercontent.com/71342594/217115061-40fe0b7c-eb35-491e-85e2-c75fb6c8a2ca.png)


Interactive rebase merge:
![image](https://user-images.githubusercontent.com/71342594/217116478-d535a29d-2e64-40e9-b17c-426cc5678f60.png)


When you shouldn't rebase with a remote repo:


Git reset, checkout, and revert:
1. What is Git reset?
Entered as "git reset *commit*" with the name of the commit. It resets to the commit the user enters.  
The commits that were done after the commit you reset to become orphan commits. 

2. What is the difference between hard, mixed, and soft?
Soft will keep the files and stage all changes while hard will destroy the file and changes.
Mixed, like soft, will undo the changes, but not delete them. Soft moves all these changes to the staging area, mixed will move the changes to the unstaged area.

3. What is Git checkout?
Git checkout switches the branch that you are on.
A command I use often at my job is git checkout -b which creates a new branch and then switches to that branch.

4. What is Git revert?
A safer way of of git reset. Prevents losing changes and does not create orphan commits.

5. In what ways are these commands the same and what ways are they different?
Revert and reset go to a previous commit and are used to undo changes. Reset however, deletes the commit you were on when you reset. Revert does not delete any commits.
Checkout also switches the current commit or branch you are on, but does not change the history or delete any commits.

6. When would you use reset, checkout, or revert? Why?
Git reset and git revert are to be used to go back to a previous commit. These can be helpful if you are undoing changes.
It is recommended to only use revert and not reset on public repos.
Git checkout is helpful if you are working on the same repo as someone else. You can change to a different branch and submit pull requests from that branch. Then you can merge that branch.
Checkout is also helpful to switch to a branch for QA testing.

Git reset:
![image](https://user-images.githubusercontent.com/71342594/217114759-2e4dd410-6c05-4582-8c41-5378ec7ed902.png)


Git checkout:
![image](https://user-images.githubusercontent.com/71342594/217114609-9cd62132-03e8-4f31-963c-7518bbc41bae.png)


Commit:
![image](https://user-images.githubusercontent.com/71342594/217114405-0bef62aa-605a-422a-a39f-acb2d60c9c94.png)


Git Revert:
![image](https://user-images.githubusercontent.com/71342594/217114853-3d88f704-0c30-4a89-8195-a2981f40fb1a.png)


Git submodules:
 1. What are Git submodules?
A record in one git repo that points to a commit in a different outside repo. 

 2. When would you use a submodule?
When you have a file that is not updated often. Or if you are trying to stay on a certain version, you can have a submodule that leads to a specific commit.

 3. What are the advantages and disadvantages of Git submodules?
It allows for projects to rely on other commits as a dependency statically, meaning the dependency would not change. Track history of external code.
It can be confusing and lead to issues. Updates to the external code are not automatically updated.
