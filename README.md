goxc
====

goxc is a cross-compilation utility for Go programs, written in Go but using *os.exec()* to call 'go build'.

goxc inspired by Dave Cheney's Bash script [golang-crosscompile](https://github.com/davecheney/golang-crosscompile).
BUT, goxc crosscompiles to all platforms at once. The artifacts are saved into a folder structure.

Pre-requisites
--------------
At this stage you still need to:

 1. Use Linux (I haven't tested on other platforms)
 2. Download the go source code and set up the GOROOT accordingly.

Basic Usage
-----------

 1. To build the toolchains for all platforms:

  go goxc.go -t

 2. To build binaries for your library:

  go goxc.go path/to/library

 Or using the binary:

  goxc path/to/library

 Or use 'goxc -h' for more options

Outcome
-------

Artifacts generated into:

 $GOBIN/appname/$GOOS/$GOARCH/latest/appname(.exe?)

Todo
----

 * 'specify artifact folder' option
 * 'generate Downloads page' option
 * 'download golang source' option?

See also
--------

See [my golang-crosscompile fork](https://github.com/laher/golang-crosscompile) for an added 'build-all' task similar to goxc.