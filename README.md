Usage
=====
    
Create folder

    mkdir aosp

Then

    cd aosp
    
initialize repo:

    repo init -u https://github.com/PixelExperience/manifest -b oreo-mr1
    
sync repo:

    $ repo sync  -f --force-sync --no-clone-bundle
    

---------------
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/aosp/aosp_manifest.xml > ~/aosp/.repo/local_manifests/roomservice.xml

sync repo:

    $ repo sync  -f --force-sync --no-clone-bundle

build AOSP (Oreo)
build:

    . build/envsetup.sh
    brunch honami
    
    
    
    
---------------------------------------------------------------------------------------------------------
build TWRP



download manifest: 

    curl https://raw.githubusercontent.com/Raschad/manifest-1/master/honami_twrp.xml > /your_directory/.repo/local_manifests/honami_twrp.xml

sync repo:

    $ repo sync

build:

    . build/envsetup.sh
    lunch

choose **aicp_honami-eng** here!
    
    mka recoveryimage
