[![Go Report Card](https://goreportcard.com/badge/github.com/cameronbrill/go-project-template)](https://goreportcard.com/report/github.com/cameronbrill/go-project-template)
[![GoDoc](https://godoc.org/github.com/cameronbrill/go-project-template?status.svg)](https://godoc.org/github.com/cameronbrill/go-project-template)

# graphite demo (record zoom)
demoing graphite.dev to my team.


### steps
- open [#1](https://github.com/cameronbrill/graphite-demo/pull/1) and [#2](https://github.com/cameronbrill/graphite-demo/pull/2) in graphite
- open [#3](https://github.com/cameronbrill/graphite-demo/pull/3) and [#4](https://github.com/cameronbrill/graphite-demo/pull/4) in github new tabs
- open [#7](https://github.com/cameronbrill/graphite-demo/pull/7), merge it
- update the graphite PRs:
```
gt co update-two
gt sync
gt restack
* resolve conflicts *
gt s
```
- observe merge conflicts are gone on both graphite PRs.

- update the vanilla PRs:
```
git checkout update-one-point-five
git rebase main
* resolve conflicts *
git push --force
git checkout update-two-point-five
git rebase update-two-point-five
* resolve conflicts again *
git push --force
```
- observe merge conflicts are gone on the two regular PRs
