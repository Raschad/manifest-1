Usage
=====
    
Create folder

    mkdir dotos

Then

    cd dotos
    
initialize repo:

    repo init -u git://github.com/DotOS/manifest.git -b dot-o
    
sync repo:

    $ repo sync  -f --force-sync --no-clone-bundle
    

---------------
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/dot/dot_manifest.xml > ~dotos/.repo/local_manifests/dot_manifest.xml

sync repo:

    $ repo sync  -f --force-sync --no-clone-bundle

build DotOS (Oreo)
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
