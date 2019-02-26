Usage
=====
navigate into desired directory
    
    mkdir mk
    cd mk
    
initialize repo:

    repo init -u https://github.com/MoKee/android.git -b mkp


Local manifest
---------------
       
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/mk-pie/roomservice.xml > ~/mk/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync

build Mokee (Pie)

    . build/envsetup.sh
    lunch
    mka bacon
