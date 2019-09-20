LineageOS 17.0 (Android 10.0) and Local manifests for Xperia Z1 (Honami)
=====

Repo sync
=====
Navigate into desired directory
    
    mkdir los
    cd los
    
Initialize repo:

    repo init -u git://github.com/LineageOS/android.git -b lineage-17.0

Create local_manifests folder
---------------
    mkdir .repo/local_manifests
    
Download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/lineage-17.0/roomservice.xml > ~/los/.repo/local_manifests/roomservice.xml

Sync repo:

    repo sync -j32

Build:

    . build/envsetup.sh
    make honami
