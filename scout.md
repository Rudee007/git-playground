## The scout Pattern: this is a part of scout pattern

### When to use:
**if we un-clear about on exactly what `git merge` will does in that case we can use this**

---

- assume this part is a new feature that we are creating

- Create a new branch in which we are implimenting feature 

- do the merge after everything done

- create a new test merge

- switch to that testing branch and do the merge.

- if the merge is succesfull then:
        
        - move your real branch forward to where the test_merge branch is.

        - `git checkout master`
        - `git merge test_merge`

- else: delete the test merge branch.

        - `git checkout master`
        - `git branch -D test-merge`