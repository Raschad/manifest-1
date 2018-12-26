Usage
=====
navigate into desired directory
    
    mkdir pixel
    cd pixel
    
initialize repo:

    repo init -u https://github.com/PixelExperience/manifest -b oreo-mr1

build Pixys (Oreo)
---------------
    mkdir .repo/local_manifests

download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/pixel/pixel_manifest.xml > ~/pixel/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync

build:

    . build/envsetup.sh
    brunch honami

