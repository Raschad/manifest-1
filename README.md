Usage
=====
navigate into desired directory
    
    mkdir pixel
    cd pixel
    
initialize repo:

    repo init -u https://github.com/PixelExperience/manifest -b pie


Local manifest
---------------
       
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/pixel-pie/roomservice.xml > ~/pixel/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync -c -j32 --force-sync --no-clone-bundle --no-tags

build Pixel Experience (Pie)

    . build/envsetup.sh
    lunch
    mka bacon -j4
---------------------------------------------------------------------------------------------------------------------------------------
For FMRadio
    
    sudo nano .repo/manifests/snippets/pixel.xml
and delete line  

project path="packages/apps/FMRadio" name="LineageOS/android_packages_apps_FMRadio" 
