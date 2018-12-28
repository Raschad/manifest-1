Usage
=====
navigate into desired directory
    
    mkdir aicp
    cd aicp
    
initialize repo:

    repo init -u https://github.com/AICP/platform_manifest.git -b p9.0

build AICP 14.0 (PIE)
---------------
    mkdir .repo/local_manifests

download manifest: 

    curl https://raw.githubusercontent.com/raschad/manifest-1/aicp-pie/aicp_manifest.xml > ~/aicp/.repo/local_manifests/aex_manifest.xml

sync repo:

    repo sync

build:

    . build/envsetup.sh
    brunch honami
