AOSP EXTENDED (Android 9.0) and Local manifests for Xperia Z1 (Honami), Xperia Z1 Compact (Amami) and Xperia Z2 (Sirius)

Repo sync
=====
Navigate into desired directory
    
    mkdir aosp
    cd aosp
    
Initialize repo:

    repo init -u git://github.com/AospExtended/manifest.git -b 9.x

Create local_manifests folder
---------------
    mkdir .repo/local_manifests
    
Download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/aex-pie/aex_manifest.xml > ~/aosp/.repo/local_manifests/roomservice.xml

Sync repo:

    repo sync -j32

Build:

    . build/envsetup.sh
    lunch
    mka aex -j4
