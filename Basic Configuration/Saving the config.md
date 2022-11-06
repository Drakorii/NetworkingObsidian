There are two system files that store the device configuration:

-   **startup-config** - This is the saved configuration file that is stored in NVRAM. It contains all the commands that will be used by the device upon startup or reboot. Flash does not lose its contents when the device is powered off.
-   **running-config** - This is stored in Random Access Memory (RAM). It reflects the current configuration. Modifying a running configuration affects the operation of a Cisco device immediately. RAM is volatile memory. It loses all of its content when the device is powered off or restarted.

To display the running-config on a device you can run:
Switch# show running-config

To display the startup-config on a device you can run:
Switch# show startup-config

To copy the running-config to the startup-config:
Switch#**copy running-config startup-config**

Note: Often times in a classroom environment you are required to **not**
save the running-config into the startup-config to make it easier for the next student
to work on the same device

