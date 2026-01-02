## savepoint experiment


- make sure you are on the right branch and that you have a clean working state

==after this  line everything comes into the main and we can test the savepoint thing==

- create a new branch to use as a savepoint, but don't switch to it.

    `git branch savepoint`

- after doing some commit or implimenting what we want in the main do the merge with the savepoint.

    `git merge savepoint`

- if everything right, we are happy with the result

    - if YES: delete the savepoint
        `git branch -d savepoint`

    - if NO:  reset your branch to the savepoint
        `git reset --hard savepoint`