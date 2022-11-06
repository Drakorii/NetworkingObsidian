To see what IP addresses are and how they are used refer to: [[IP Addresses]]

To configure a ipv4 address on any device and interface:
Sw-Floor-1# **configure terminal** 
Sw-Floor-1(config)# **interface vlan 1** 
Sw-Floor-1(config-if)# **ip address 192.168.1.20 255.255.255.0** 
Sw-Floor-1(config-if)# **no shutdown** 
Sw-Floor-1(config-if)# **exit**
Sw-Floor-1(config)# **ip default-gateway 192.168.1.1**