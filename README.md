Usage
=====
navigate into desired directory

    mkdir aicp
    cd aicp
initialize repo:

    repo init -u https://github.com/AICP/platform_manifest.git -b o8.1

build AICP 13.1 (Oreo)
---------------
    mkdir .repo/local_manifests
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/master/roomservice.xml > ~/aicp/.repo/local_manifests/roomservice.xml


build LOS 16.0 (pie)
---------------
download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/master/honami_lineage-16.0 > ~/los/.repo/local_manifests/roomservice.xml

sync repo:

    repo sync -c -j32 --force-sync --no-clone-bundle --no-tags

build:

    . build/envsetup.sh
    brunch honami
