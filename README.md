# RarFS - Fuse extension for mounting rar files

RarFS is a Fuse module for mounting an uncompressed rar archive as a filesystem. This is a good idea for eg. video streaming where the media file is in a rar archive and you don't want to use a lot of extra diskspace, and time, for extracting and then streaming.

## Build dependencies
* libfuse-dev

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

## Use

When you have installed rarfs on your machine, you´re ready to use it.
Use the following commands to mount a rar file on a specified mount point.

```bash
mount.fuse rarfs# /my/rarfile.rar /my/mountpoint
```

To unmount the rar file from the mountpoint, execute the following

```bash
fusermount -u /my/mountpoint
```
