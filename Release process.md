How to release:

Current release process is pretty much easy (may not look professional but hey!)

Steps:

1. Run the `sagittarius-release.sh`
2. Create Windows installer with the source directory created above step. (both 32 and 64 bits)
3. Write release notes on bitbucket.org wiki
4. Upload tar ball and installers
5. Update documents on GitHub

As an extra step, we also build the tar ball on couple of Linux environments if possible.

`sagittarius-release.sh`
```
#!shell
#!/bin/sh

SRC_DIR=sagittarius.dist
WORK_DIR=build
#
rm -rf $SRC_DIR
hg clone https://ktakashi@bitbucket.org/ktakashi/sagittarius-scheme $SRC_DIR
cd $SRC_DIR
./dist.sh gen
cd ../

rm -rf $WORK_DIR
mkdir $WORK_DIR
cd $WORK_DIR
cmake ../$SRC_DIR
make
make doc
make online-doc
make test
make install -j 8
../$SRC_DIR/dist.sh dist ../$SRC_DIR
```