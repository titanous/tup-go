1. Install tup and Go.
1. Create a directory and export the `GOPATH` environment variable pointing to
   it.
1. Clone this repo into `$GOPATH/src/github.com/titanous/tup-go`.
1. Run `tup`.
1. `touch foo/bar.go`
1. Run `tup` again and note that `tup-go` isn't rebuilt.
1. Run `tup graph . | dot -Tpng > deps.png` and note that `foo/bar.go` is not an input
   to anything.
1. Run `go build -x` and note that `foo/bar.go` is read by `6g`.
