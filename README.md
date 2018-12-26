Usage
=====
navigate into desired directory
    
    mkdir du
    cd du
    
initialize repo:

    repo init -u https://github.com/DirtyUnicorns/android_manifest -b o8x-caf

build Dirty Unicorns (Oreo)
---------------
    mkdir .repo/local_manifests

download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/du-oreo/du_manifest.xml > ~/du/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync

build:

    . build/envsetup.sh
    brunch honami

