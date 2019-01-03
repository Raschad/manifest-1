Usage
=====
navigate into desired directory
    
    mkdir superior
    cd superior
    
initialize repo:

    repo init -u git://github.com/SuperiorOS/manifest.git -b pie

build Superior OS (Pie)
---------------
    mkdir .repo/local_manifests
    
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/superior-pie/superior_manifest.xml > ~/superior/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync -c -j32 --force-sync --no-clone-bundle --no-tags

build:

    . build/envsetup.sh
    brunch honami
