## How to Resolve Merge Conflicts

### What is a Merge Conflict?

A conflict happens when two branches modify the same line of code and Git  
cannot decide which one to keep.

### Steps to Resolve Conflict

Pull or rebase latest changes

Git shows conflicted files

Open the file and look for markers:

```text
<<<<<<< HEAD
your code
=======
other code
>>>>>>> main
Decide final code and remove markers

Mark conflict as resolved:

bash
Copy code
git add <file-name>
Complete merge or rebase:

bash
Copy code
git commit
# or
git rebase --continue