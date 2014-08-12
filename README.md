GoSass
======

A fork of the official [gosass](https://github.com/moovweb/gosass) repo to fix cgo library and include paths for building.

Gosass is a language wrapper for LibSass (the C/C++ implementation of Sass).

For sample usage, see the file `gosass.go`. But make sure you move it to a different folder or comment it out before building, because the Go build tools don't like having two separate modules in the same folder!

### Building

To use in your Go programs, get the libsass code (including submodules) into a folder somewhere. Then run

CGO_CFLAGS="-I$PWD/lib/libsass" CGO_LDFLAGS="-L$PWD/lib/libsass" go run main.go (or whatever)


