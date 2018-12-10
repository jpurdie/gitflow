# Git Flow
## I want to...
### ...create a new branch.
1. Switch to the branch you want to copy

    ```sh
    $ git checkout <existingBranchName>
    ```

2. Create new local branch

    ```sh
    $ git checkout -b <newBranchName>
    ```
3. Push branch to remote server

    ```sh
    $ git push --set-upstream origin <newBranchName>
    ```

### ...switch to a branch.
1. Switch to existing branch

    ```sh
    $ git checkout <branchName>
    ```
2. Always a good idea to update with origin

    ```sh
    $ git pull
    ```    

### ...make changes to a branch.
1. Commit changes to branch (local)

    ```sh
    $ git commit -am 'commit comments'
    ```
2. Push changes to remote server

    ```sh
    $ git push
    ```

### ...merge production into a branch
1. Checkout develop & pull latest

    ```sh
    $ git checkout develop
    $ git pull
    ```
2. Checkout feature branch

    ```sh
    $ git checkout <branchName>
    ```
3. Merge develop into feature branch, commit, and push to remote server

    ```sh
    $ git merge develop
    $ git commit -am 'merging production'
    $ git push
    ```


### ...mark production release.
1. Checkout develop and make sure you have the latest

    ```sh
    $ git checkout develop
    $ git pull
    ```
2. Merge feature branch that is going live into develop & push to remote server

    ```sh
    $ git merge <branchName>
    $ git push
    ```

4. Delete feature branch locally and remote

    ```sh
    $ git branch -d <branchName>
    $ git push origin --delete <branchName>
    ```
5. Merge changes into master branch

    ```sh
    $ git checkout master
    $ git merge develop
    $ git push
    ```
6. View list of existing tags

    ```sh
    $ git tag
    ```
7. Mark with new tag (usually by incrementing 1) and push to remote server

    ```sh
    $ git tag -a <newTag> -m 'commit comments'
    $ git push --tags
    ```
