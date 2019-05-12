LineageOS
=====

Usage
=====
navigate into desired directory
    
    mkdir los
    cd los
    
initialize repo:

    repo init -u git://github.com/LineageOS/android.git -b lineage-16.0


Local manifest
---------------
       
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/lineage-16.0/roomservice.xml > ~/los/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync -j 32

build LineageOS 16.0 (Pie)

    . build/envsetup.sh
    brunch sirius

---------------------------------------------------------------------------------------------------------------------------------------
For FMRadio
    
    sudo nano .repo/manifests/snippets/lineage.xml
and delete line 39   
project path="packages/apps/FMRadio" name="LineageOS/android_packages_apps_FMRadio" 
   
 
