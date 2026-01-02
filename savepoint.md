## savepoint experiment

### When to use:
**when we know what we want to impliment but just want to add a undo button in case things get too comlicated.**

---

- make sure you are on the right branch and that you have a clean working state

<mark>after this  line everything comes into the main and we can test the savepoint thing and the steps of using savepoint pattern</mark>

- create a new branch to use as a savepoint, but don't switch to it.

    `git branch savepoint`

- after doing some commit or implimenting what we want in the main do the merge with the savepoint.

    `git merge savepoint`

- if everything right, we are happy with the result

    - if YES: delete the savepoint
        `git branch -d savepoint`

    - if NO:  reset your branch to the savepoint
        `git reset --hard savepoint`

#### note:

<mark>what really happen is:<mark>

**main is moved to point at savepoint.**
```
A -- B -- C -- D (main)

```

- we run:

```
git reset --hard B   # B = savepoint

```

- result: 

```
A -- B (main)
```