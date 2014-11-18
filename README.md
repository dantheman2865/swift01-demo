swift01-demo
============

Demo application(s) for the Swift01 module:

COORD is the master device and issues a beacon message about once per second.
DEV is the device and echoes the beacon back to the host.

These examples have been modified such that the device reads a GPIO to get a switch state and broadcasts a message (address and PAN ID 0xFFFF) with the switch state.

When the coordinator receives the broadcast message, it matches a GPIO output to that message (which I used to control a relay).

All of the MAC and PHY software is Atmel's ASF packages for 802.15.4 MAC and PHY.
