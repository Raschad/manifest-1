Usage
=====
navigate into desired directory
    
    mkdir aosp
    cd aosp
    
initialize repo:

     repo init -u https://github.com/ArrowOS/android_manifest.git -b arrow-9.x


Local manifest
---------------
       
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/arrow-pie/roomservice.xml > ~/aosp/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync -c -j32 --force-sync --no-clone-bundle --no-tags

build Arrow ROM (Pie)

    . build/envsetup.sh
    brunch honami
