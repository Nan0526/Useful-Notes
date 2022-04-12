# 在一个branch里面新加的file同时出现在了其他branch里面

If you git add a file, but then switch branches before committing, the staged addition will be carried over to the new branch (just like any other staged changes). **You probably wanted to commit before switching branches.**

Any uncommitted changes, including files that are not added to the repository, are preserved when switching the working copy between branches.

Just making a new file does not automatically add it to the repository, you have to do a git add myFile (and eventually commit that).

Or, looking at it the other way, even if the file stays around in your working copy when you switch branches, it won't become part of those other branches unless you explicitly add and commit them there, either.


# Git rebase --skip all 
有时候太久没有rebase，然后有很多conflicts, 而且我们只需要选择HEAD的commit. 所以就可以用这个command:   
`while [ true ]; do git rebase --skip; if [ $? -eq 0 ]; then break; fi; done`
