# cross-lfs-multilib
Scripts to build multilib Linux From Scratch (based on CLFS and LFS)

### How to use:

0. Create `cross-tools` and `lfs` dir.
       
       
       sudo mkdir -p /mnt/lfs
       sudo mkdir -p /mnt/lfs/cross-tools
       sudo mkdir -p /mnt/lfs/tools
       sudo ln -sv /mnt/lfs/tools /
       sudo ln -sv /mnt/lfs/cross-tools /
       

1. Run ./fetch-sources to download all needed sources

       ./fetch-sources
       
2. create $LFS directory (`/mnt/lfs` is default, you can change it in `build-properties`)

       sudo mkdir -v /mnt/lfs

3. create `$LFS/tools` and symlink it to root directory (/)

       sudo mkdir -v /mnt/lfs/tools
       sudo ln -sv /mnt/lfs/tools /

4. change perm/owner of `/mnt/lfs/tools` to your user (change `emmett` to your user)

       sudo chown -v emmett:emmett /mnt/lfs/tools

5. run ./strap to build the toolchain

       ./strap
