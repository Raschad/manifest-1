Usage
=====
navigate into desired directory
    
    mkdir pixys
    cd pixys
    
initialize repo:

    repo init -u https://github.com/PixysOS/manifest -b oreo

build Pixys (Oreo)
---------------
    mkdir .repo/local_manifests

download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/pixys/pixys_manifest.xml > ~/pixys/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync

build:

    . build/envsetup.sh
    brunch honami

