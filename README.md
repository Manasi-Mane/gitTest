# Git Basics Practice

\## Handling Mistakes Safely



I intentionally committed a file (`mistake.txt`) that shouldn't have been added.



\*\*Command used:\*\* `git reset --soft HEAD\~1`



\*\*Why:\*\* Since the mistaken commit had not yet been pushed to the remote repository,

it was safe to use `reset --soft`, which removes the commit from history but keeps

the changes staged. This let me review and discard the unwanted file cleanly without

leaving any trace in the commit history. `git revert` would be the better choice if

the commit had already been pushed and shared with others, since it preserves history

by adding a new "undo" commit instead of rewriting existing history.

