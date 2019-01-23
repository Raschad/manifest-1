Usage
=====
navigate into desired directory
    
    mkdir rr
    cd rr
    
initialize repo:

    repo init -u https://github.com/ResurrectionRemix/platform_manifest.git -b pie


Local manifest
---------------
       
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/rr-pie/roomservice.xml > ~/rr/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync

build Resurrection Remix (Pie)

    . build/envsetup.sh
    brunch honami 

or

    brunch amami
