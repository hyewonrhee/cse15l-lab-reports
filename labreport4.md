# Lab Report 4

## Hye Won Rhee

**Step 1: Log into ieng6**

![Screenshot1](/cse15l-lab-reports/LR4-1.png)

Keys pressed: `ssh`, and then my ieng6 account username, then `<enter>`.

**Step 2: Clone fork**

![Screenshot2](/cse15l-lab-reports/LR4-2.png)

Keys pressed: `git clone`, then pasted the `SSH` URL of the repository fork from my GitHub account, then `<enter>`.

The `lab7` directory already existed, so I used the `rm` command to remove it in order to properly clone the repository.

**Step 3: Run the tests (should fail)**

![Screenshot3](/cse15l-lab-reports/LR4-3.png)

Keys pressed: `bash`, then `test.sh`, then `<enter>`.

I misspelled `test.sh` at first, so I pressed `Ctrl-W` to delete the last word and retype it correctly.

**Step 4: Edit the code to fix failing test**

![Screenshot4](/cse15l-lab-reports/LR4-4.png)

Keys pressed: `vim`, then name of the file I want to edit, which was `ListExamples.java`, then `<enter>`.

When actually editing the file, I pressed `<j>` to move the cursor down, `<l>` to move it right, `<x>` to delete the intended character,
`<i>` to insert the replacement character (`<2>`), then `esc` to exit from insert mode and enter Normal Mode, then finally `<:wq>` to
save the change I made and exit the editor.

**Step 5: Run the tests (should succeed)**

![Screenshot5](/cse15l-lab-reports/LR4-5.png)

Keys pressed: `Ctrl-R`, then I typed `ba` to search for a command I used in the past, and it was autofilled with `bash test.sh` from Step 3.

Then I hit `<enter>`, and the command was used to run the tests once again, which succeeded with the change I made through `vim`.

**Step 6: Commit and push the change to GitHub account**

![Screenshot6](/cse15l-lab-reports/LR4-6.png)

Keys pressed: `git add`, then name of existing file with changes, `ListExamples.java`.

Then, `git status` to check the state of the working directory and to make sure this change to `ListExamples.java` is being tracked.

![Screenshot7](/cse15l-lab-reports/LR4-7.png)

Keys pressed: `git commit -m`, then a commit message detailing what edit I made to the repository, which was `edited ListExamples.java`.

![Screenshot8](/cse15l-lab-reports/LR4-8.png)

Keys pressed: `git push`, in order to transfer the commit I just added, from local to remote.

![Screenshot9](/cse15l-lab-reports/LR4-9.png)

Showing that the change was correctly committed and pushed to the repository.
