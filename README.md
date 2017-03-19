Device repository for Doogee Y100 Pro (Lineage)
==========================

Getting Started
---------------

Initialize a repository with CyanogenMode:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-14.1
    
Sync sources:    

    repo sync
    
Build the code:
    
    cd device
    mkdir y100pro
    cd y100pro
    git clone https://github.com/bolt1502/android_device_y100pro_persimmon_3_10_65.git persimmon
    cd persimmon/patches
    . apply-patches.sh
    cd vendor
    mkdir y100pro
    cd y100pro
    git clone https://github.com/olegsvs/android_vendor_y100pro_persimmon_3_10_65 persimmon
    cd ../../
    source build/envsetup.sh
    breakfast persimmon
    make -j 4 bacon

Current state
-------------

- Cyanogen boots
- Touch, screen, keyboard working
- Wifi is working
- Audio is working
- Telephony is working (see Known Issues)
    - USIM (3G) supported
    - Incoming/outgoung call
    - SMS, USSD
    - Data connectivity
- GPS
- Bluetooth (pairing only testes so far)
- Sensors

Known Issues
-------------
- Livedisplay (lagging)
- FMRadio
- VoLTE
- Gps without network connections?
- Camera
- Hardware OMX codecs are not working
