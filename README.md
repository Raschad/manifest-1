Usage
=====
navigate into desired directory
    
    mkdir aosp
    cd aosp
    
initialize repo:

    repo init -u git://github.com/AOSiP/platform_manifest.git -b pie

build AOSIP (Pie)
---------------
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/aosip-pie/roomservice.xml > ~/aosp/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync

build:

    . build/envsetup.sh
    lunch
    time mka kronic
