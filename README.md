Usage
=====
navigate into desired directory
    
    mkdir dot
    cd dot
    
initialize repo:

    repo init -u git://github.com/DotOS/manifest.git -b dot-p

build DOT OS (Pie)
---------------
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/dot-9/dot_manifest.xml > ~/dot/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync -c -j32 --force-sync --no-clone-bundle --no-tags

build:

    . build/envsetup.sh
    brunch honami
