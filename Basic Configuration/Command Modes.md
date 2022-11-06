As a security feature, the Cisco IOS software separates management access into the following two command modes:

-   **User EXEC Mode** - This mode has limited capabilities but is useful for basic operations. It allows only a limited number of basic monitoring commands but does not allow the execution of any commands that might change the configuration of the device. The user EXEC mode is identified by the CLI prompt that ends with the > symbol.
-   **Privileged EXEC Mode** - To execute configuration commands, a network administrator must access privileged EXEC mode. Higher configuration modes, like global configuration mode, can only be reached from privileged EXEC mode. The privileged EXEC mode can be identified by the prompt ending with the # symbol.
    - Global configuration mode (Targets the whole device)
    - Interface configuration mode (Targets specified interfaces)


If you start up a switch it will look like this:
Switch>

Which is the user EXEC mode. To get into privileged EXEC mode you have to type:
Switch> **enable**
Switch# **disable**
Switch>

If you want to go into global configuration mode:
Switch>**enable**
Switch# **configure terminal**
Switch(config)# **exit**
Switch# **disable**
Switch>

If you want to go into the interface config mode:
Switch> **enable**
Switch# **configure terminal**
Switch(config)# **interface fa0/0**
Switch(config-if# **exit**
Switch(config)# **exit**
Switch# **disable**
Switch>

If you want to configre multiple interfaces at once:
Switch> **enable**
Switch# **configure terminal**
Switch(config)# **interface fa0/0-15**
Switch(config-if# **exit**
Switch(config)# **exit**
Switch# **disable**
Switch>