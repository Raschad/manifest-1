Usage
=====
navigate into desired directory
    
    mkdir aosp
    cd aosp
    
initialize repo:

    repo init -u git://github.com/crdroidandroid/android.git -b 9.0

build CrDroid (Pie)
---------------
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/cr-pie/roomservice.xml > ~/aosp/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync

build:

    . build/envsetup.sh
    brunch honami
---------------------------------------------------------------------------------------------------------------------------------------
For FMRadio
    
    sudo nano .repo/manifests/snippets/lineage.xml
and delete line 39   
project path="packages/apps/FMRadio" name="LineageOS/android_packages_apps_FMRadio" 
   
