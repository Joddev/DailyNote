#### 여러 commits 하나로 합치기

`rebase -i <HEAD>`

```bash
pick HEAD1 log1
pick HEAD2 log2

# Rebase 326fc9f..0d4a808 onto d286baa
#
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
#
# If you remove a line here THAT COMMIT WILL BE LOST.
# However, if you remove everything, the rebase will be aborted.
#
```

#### 이미 커밋된 파일 ignore하기

1. Edit `.gitignore`
2. `git rm --cached /path/to/file`

