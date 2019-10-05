AOSP EXTENDED (Android 10.0) and Local manifests for Xperia Z1 (Honami)
=====

Repo sync
=====
Navigate into desired directory
    
    mkdir aosp
    cd aosp
    
Initialize repo:

To initialize your local repository using the AospExtended trees, use a command like this:

    repo init -u git://github.com/AospExtended/manifest.git -b 10.x
To initialize a shallow clone, which will save even more space & time, use a command like this:

    repo init --depth=1 -u git://github.com/AospExtended/manifest.git -b 10.x

Create local_manifests folder
---------------
    mkdir .repo/local_manifests
    
Download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/aex-10/roomservice.xml > ~/aosp/.repo/local_manifests/roomservice.xml

Sync repo:

    repo sync -j32
    
    repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

Build:

    . build/envsetup.sh
    brunch honami
