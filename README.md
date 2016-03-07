# RarFS - Fuse extension for mounting rar files

## Build dependencies
libfuse

## Build

To do a simple build, use these commands:

```bash
# Generates configure script and Makefile.in files; copy ltmain.sh
autoreconf --verbose --install

./configure
make
make install
```

To generate a release tarball, run

`fakeroot make distcheck`

