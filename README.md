Usage
=====
navigate into desired directory
    
    mkdir aosp
    cd aosp
    
initialize repo:

    repo init -u git://github.com/AospExtended/manifest.git -b 9.x

build Aosp Extended (Pie)
---------------
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/aex-pie/aex_manifest.xml > ~/aosp/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync

build:

    . build/envsetup.sh
    brunch honami
