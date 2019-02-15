Usage
=====
navigate into desired directory
    
    mkdir aosp
    cd aosp
    
initialize repo:

    repo init -u git://github.com/ancient-rom/manifest.git -b pie

build Ancient-ROM (Pie)
---------------
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/ancient-pie/roomservice.xml > ~/aosp/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync --current-branch --no-tags --no-clone-bundle --optimized-fetch --force-broken --force-sync -j32

build:

    . build/envsetup.sh
    lunch
    mka bacon -j4
