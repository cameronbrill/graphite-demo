[![Go Report Card](https://goreportcard.com/badge/github.com/cameronbrill/go-project-template)](https://goreportcard.com/report/github.com/cameronbrill/go-project-template)
[![GoDoc](https://godoc.org/github.com/cameronbrill/go-project-template?status.svg)](https://godoc.org/github.com/cameronbrill/go-project-template)

# graphite demo (record zoom)
demoing graphite.dev to my team.


### steps
- open [#8](https://github.com/cameronbrill/graphite-demo/pull/8), [#9](https://github.com/cameronbrill/graphite-demo/pull/9), [#10](https://github.com/cameronbrill/graphite-demo/pull/10) in graphite
- open [#13](https://github.com/cameronbrill/graphite-demo/pull/13), [#14](https://github.com/cameronbrill/graphite-demo/pull/14), [#15](https://github.com/cameronbrill/graphite-demo/pull/15) in github
- open [#11](https://github.com/cameronbrill/graphite-demo/pull/11) and [#12](https://github.com/cameronbrill/graphite-demo/pull/12) in graphite. merge them.
- update the graphite PRs:
```
gt co main
gt sync
gt co print-single-hello-world
gt restack
* resolve conflicts *
gt s
```
- observe merge conflicts are gone on the graphite PRs.

- update the vanilla PRs:
```
git checkout print-single-hello-world-2
git rebase main
* resolve conflicts *
git push --force
git checkout upgrade-print-function-2
git rebase print-single-hello-world-2
* resolve conflicts again *
git push --force
git checkout print-num-input-2
git rebase upgrade-print-function-2
* resolve conflicts again *
git push --force
```
- observe merge conflicts are gone on the three regular PRs
