# How to share your stashes





## 1)  Include untracked files

```bash
git ls-files -o > files-to-untrack
git add `cat files-to-untrack` # note: files-to-untrack will be listed, itself!
git stash
# do some work
git stash pop
git rm --cached `cat files-to-untrack`
rm files-to-untrack
```



## 2) Create a stash

```bash
id=`git stash create`
git stash save $id
git push stash@{0}:refs/stashes/0
```

