Usage
=====
navigate into desired directory
    
    mkdir omni
    cd omni
    
initialize repo:

    repo init -u git://github.com/omnirom/android.git -b android-9.0

build Omni ROM (Pie)
---------------
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/omni-pie/roomservice.xml > ~/omni/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync

build:

    . build/envsetup.sh
    brunch honami
