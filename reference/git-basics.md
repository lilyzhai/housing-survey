# Git Refresher

## Some Comments
Two people should never be working on the same branch at the same time, unless they have each created their own sub-branches! Instead, try to pair program and maybe switch every so often. In general, branches should be short-lived; the probability of making a fatal error increases drastically the longer it's been without a merge. Long branches are ok if they are guaranteed to be independent from any other branches that you may need to create later.

## General Workflow
https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository

**ALWAYS ```git pull``` to fetch new changes before you push anything!**

Let's say you're working on a branch and you are ready to push your files to Git.
The process has three steps.

1. First, run the following to **stage** all your changes:

      ```git add .```

2. Then, **commit** your changes to your local directory. 

      ```git commit -m "MESSAGE"```

3. Push your changes to the remote directory.

      ```git push```
      
      
## Branches
https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging

The way Git works, we want to be able to work independently on different parts of the project and merge them back in later. Note, **any two branches should be independent**; modifying the same file in two branches could (and probably will) result in a merge conflict. These are bad.

To create a branch:
    
    git checkout -b <BRANCH_NAME>
     
Do some work in that branch; you won't be able to push any changes if you don't have any!
Then, you'll stage and commit your changes. Finally:

    git push -u origin <BRANCH_NAME>
    
**NOTE**: you only have to do the above the first time you push changes just so Git knows where to push the changes to. Otherwise, ```git push``` will work fine.

When you are completely done working, you can try to merge the branch back into Git by issuing a **pull request**. We'll just do this on Github instead of from the command line, since these are risky.

## Resolving conflicts
Let's hope I don't have to write this section!

