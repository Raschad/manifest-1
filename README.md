Usage
=====
navigate into desired directory

initialize repo:

    repo init -u https://github.com/AICP/platform_manifest.git -b o8.1

build AICP 13.1 (Oreo)
---------------
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/dot/dot_manifest.xml > ~dotos/.repo/local_manifests/dot_manifest.xml

sync repo:

    $ repo sync

build:

    . build/envsetup.sh
    brunch honami

build TWRP
----------
download manifest: 

    curl https://raw.githubusercontent.com/Raschad/manifest-1/master/honami_twrp.xml > /your_directory/.repo/local_manifests/honami_twrp.xml

sync repo:

    $ repo sync

build:

    . build/envsetup.sh
    lunch

choose **aicp_honami-eng** here!
    
    mka recoveryimage
