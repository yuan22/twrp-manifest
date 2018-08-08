## Getting Started ##
---------------

To get started with OMNI sources to build TWRP, you'll need to get
familiar with [Git and Repo](https://source.android.com/source/using-repo.html).

To initialize your local repository using the OMNIROM trees to build TWRP, use a command like this:

    repo init -u git://github.com/hejsekvojtech/twrp-manifest.git -b android-8.1
    
To initialize a shallow clone, which will save even more space, use a command like this:

    repo init --depth=1 -u git://github.com/hejsekvojtech/twrp-manifest.git -b android-8.1

Then to sync up:

    repo sync

Then to build:

     export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch omni_<device>-eng; mka recoveryimage

