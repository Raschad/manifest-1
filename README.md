Usage
=====
    
Create folder

    mkdir pix

Then

    cd pix
    
initialize repo:

    repo init -u https://github.com/PixysOS/manifest -b pie
    
sync repo:

    $ repo sync  -f --force-sync --no-clone-bundle
    

---------------
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/pixys_pie/aosp_manifest.xml > ~/pix/.repo/local_manifests/pixys.xml

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
