# Ignored Files

## Reason why this may be useful

Use this when you get changes to files that you did not do but can't add them to .gitignore because they may get modified by others.

## References

* Came across this in my initial investigation of trying to solve my problem.
  https://hackernoon.com/exclude-files-from-git-without-committing-changes-to-gitignore-986fa712e78d

* Had the git command I was looking for.
  http://codethug.com/2013/09/20/4-ways-to-ignore-files-with-git/

* Had some good commands that were also useful after ignoring files, like show what files that were ignored.
  https://stackoverflow.com/questions/2363197/can-i-get-a-list-of-files-marked-assume-unchanged
  
* To unignore a file
  https://stackoverflow.com/questions/17195861/undo-git-update-index-assume-unchanged-file

## The commands

### Ignore a file

```
git update-index --assume-unchanged <filename>
```

### Show ignored files

```
git ls-files -v | grep '^[[:lower:]]'
```

### Git alias to show ingored files

```
ignored = !git ls-files -v | grep "^[[:lower:]]"
```

### Unignore a file

```
git update-index --no-assume-unchanged <filename>
```

## ToDo:

1. Have a command that can be copied and pasted for the alias.
