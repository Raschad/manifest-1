Usage
=====
navigate into desired directory
       
    mkdir nitrogen
    cd nitrogen

initialize repo:

    repo init -u https://github.com/nitrogen-project/android_manifest.git -b p

build Nitrogen OS (PIE)
---------------
Create local_manifests if error
    
    mkdir .repo/local_manifests

download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/nos_pie/honami.xml > ~/nitrogen/.repo/local_manifests/roomservice.xml

sync repo:

    $ repo sync

build:

    . build/envsetup.sh
    brunch honami
