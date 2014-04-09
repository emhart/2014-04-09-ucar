Branching
-----------

- Have students create a branch.

- Have student checkout branch

- Show shortcut... `git checkout -b <branchname>`

- Have students switch branches.  Make a change, commit.

- Now switch back to master.  What do they expect to see?

- Talk about branching and workflows


Merging
---------

works with `git merge [branch_name]` where branch_name is merged into current branch.

- Merge branch on to master. 

- Check out master.

- Check out other branch

- See that they are the same.

-- Exercise:

 	* Have students go ahead in both the master and their development branch.  Then ask them to merge into the master.  What happens?

- Have students push changes to github, look at branching diagram
 
- Draw picture on white boar

 Rebasing
 --------

- Create a new branch

- make several commits on master

- Make a commit on new branch.

- Go into master, make a bunch of commits

- Now go into master branch....
	`git rebase <newbranch>`

- push commits, see that they're different, all in one line


----- IF YOU HAVEN'T HAD A CONFLICT YET FORCE ONE HERE WITH MERGE ---

Resetting work
---------------

`git reset HEAD^` or ~ goes back one commit hard

`git reset --hard HEAD` goes back one commit

- Make a new set of commits
 
`git reset --soft HEAD` 

`git reset --soft <commit>` will roll back to a commit but keep your changes

`git reset --hard <commit>` will roll back to those commits and you will lose the modified file

- See how it just goes back to modified files

- But it doesn't work if you go back to what you were at.

- This is a good way to go back if you're just working locally.

- Have the students try and push. Do they get conflicts?

- Try resetting work, Try with a soft reset.  Try with a hard reset

- Now try pushing this up to github.  What happens?



`reverting`
---- 

`git revert <commit>` will merge changes from the branch and append it to your history.

Have students look at git log.  What's the difference?


-----
- Another easy way to do this is with checkout.

`git checkout -b <new branch name> <commitID>`

Now you can play around, and merge that back into master...

You can now push that up to github

---- Exercise ----

Have students go back and checkout a branch.  Then recommit back to master.  Push it up to github.


Working with remotes
-----

You can have lots of remotes

They are easy to add, we've already done this with github, but you could have others.

- see remotes with `git remote -v`

- add more with `git remote add <name> <url>`


Adding a new project
----

- Have students fork an existing project.

- Have them clone it.

- Have them make some changes, push to their repo and make a pull request

Have students do some faux collaboration

Updating your forked repo
----------------------------

-add new remote
`git remote add upstream https://github.com/emhart/test.git`
`git fetch upstream`
`git rebase upstream/master`
`git push -f origin master`

- That will force an update 
- Now your local and forked branch are up to date with the original fork.

Go over github features
-----------------

- Issues
- commit history
- markdown rendering
- viewing past commits and diff.
