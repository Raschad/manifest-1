
Repo sync
=====
Navigate into desired directory
    
    mkdir omni
    cd omni
    
Initialize repo:

    repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0

Create local_manifests folder
---------------
    mkdir .repo/local_manifests
    
Download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/twrp-android-10.0/twrp_manifest.xml > ~/omni/.repo/local_manifests/roomservice.xml

Sync repo:

    repo sync -j32

Build:

    export ALLOW_MISSING_DEPENDENCIES=true
    . build/envsetup.sh && lunch omni_honami-eng
    mka recoveryimage
