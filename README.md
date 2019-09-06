full hotpatch clover thanks to @CrazyPegasus , @宪武 and @MAJ in pcbeta forum.

video : https://www.youtube.com/channel/UCmVLJUv2nHImPS5CbaUuyKQ

## BIOS setting
  - Enabled DEP (under memory protection / execution prevention)
  - Disabled secure boot
  - Disabled legacy boot
  - Enabled CSM
  - Enabled boot from USB
  - No Fast Boot Option
  - No Data mode option
  - Intel SGX Disabled
  - TPM Disabled
  - thunderbolt bios assist : disabled
  - Sleep mode : see information below

## Working/Not working list
  - what is working
    - audio
    - Built in Camera (connected through usb)
    - brightness adjustment (via keyboard)
    - HDMI output throught type c slot and HDMI slot
    - wifi&bluetooth (swap your wifi card) [Broadcom DW1560(OEM by Dell), DW1830(OEM by Dell), BCM94352Z(OEM by Lenovo), BCM943602BAED(OEM by Lenovo), BCM94360CS2(OEM by Apple), BCM943602CS(OEM by Apple)]
    - trackpad (PS/2 synaptics trackpad , drived by acidanthera voodoops2)
    - *touchscreen*
      - connected through usb
      - ***there is two option to get multitouch and pen support for touchscreen***
        - voodooi2c.kext and voodooi2chid.kext
          - recommended : for it is free , and gesture is very responsive
          - download here https://github.com/alexandred/VoodooI2C/releases
          - support
            - touchscreen gesture : native 1~5 fingers gesture , same as trackpad gesture , you can adjust your gesture in bettertouchtool
            - stylus pen
              - upper button : act as right click
              - pen touch : act as left click
                - stylus pen pressure sensitivity is not supported
              - lower button + pen touch : act as middle click
              - bluetooth connection to your osx , use top button
                - bluetooth connection is not stable
                - three function : single press , double press , long press ; being treat as keyboard event
                - can be remapped via bettertouchtool
              - pen button function(including top button) can be adjusted via controllermate and bettertouchtool)
        - touch-base updd driver ( you can mail to them for a trial driver , for free)
          - not recommended : for higher cpu usage(about 10 percent) , occationally the touch has laggy issue , and the driver is expensive
          - support
            - touchscreen gesture : can be adjust via GUI menu
            - stylus pen
              - upper button + pen touch + lower button + bluetooth connection
              - pen touch has pressure sensitivity
              - the upper and lower button function cannot be adjusted via controllermate
    - usb type C hotplug
    - battery status (Percentage can be displayed)
    - Backlit keyboard (Use Fn + space)
    - graphics acceleration
    - Ethernet port
    - Mac App Store works normally
    - microSD card reader
      - connected through usb , therefore it works without any kext needed
    - sleep and wake
      - ***need to update to bios 1.35 or newer***
      - sleep mode
        - choose windows for modern standby : higher battery drainage , not recommended
        - choose linux for normal S3 sleep : lower battery drainage , recommended
      - when the machine is sleeping , the LED bulb will blink , after wake it become to normal
  - untest(not sure)
    - thunderbolt 3
      - do not have device , not tested ; if you have device please contact me
    - WWAN
      - do not have device , not tested ; WWAN is connected through usb , therefore you can passthrough your WWAN into virtual machine , and it will work

## Personal Customization
  - EDID & HiDPi
    - use hackintool or one-key-hidpi
  - CPU frequency
    - use one-key-cpufriend

## Reference
  - https://blog.daliansky.net
  - https://www.tonymacx86.com/threads/guide-thinkpad-x1-yoga-3rd-gen-20ld-with-mojave.261823/
  - https://github.com/Jamesxxx1997/thinkpad-x1-carbon-2018-hackintosh
  - https://github.com/daliansky/P-little
  - https://www.tonymacx86.com/threads/an-idiots-guide-to-lilu-and-its-plug-ins.260063/
  
