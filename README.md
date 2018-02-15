# usbh_midi_samd
USB Host MIDI for Arduino SAMD boards

usbh_midi_samd is the USBH_MIDI driver from the USB Host Shield 2.0 project to
the ArduinoCore-samd project.  Most of the time was spent fixing bulk in/out
pipes. A USB OTG to host cable or adapter is required.

The driver has been tested minimally on an Arduino Zero but it should
work on other boards based on the SAMD family. For example, the driver
works on an Adafruit Trinket M0.

Changes are needed to the following ArduinoCore-samd files:

* cores/arduino/USB/samd21_host.c
* libraries/USBHost/src/address.h
* libraries/USBHost/src/Usb.cpp

All of the USBH_MIDI files require trivial renaming changes.

By the way, the fix described in https://github.com/arduino/ArduinoCore-samd/issues/271 is included.
