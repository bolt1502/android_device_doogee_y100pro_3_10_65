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
    mkdir doogee
    cd doogee
    git clone https://github.com/bolt1502/android_device_doogee_y100pro_3_10_65.git y100pro
    cd y100pro/patches
    . apply-patches.sh
    cd vendor
    mkdir doogee
    cd doogee
    git clone https://github.com/bolt1502/android_vendor_doogee_y100pro_3_10_65.git y100pro
    cd ../../
    source build/envsetup.sh
    breakfast y100pro
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
