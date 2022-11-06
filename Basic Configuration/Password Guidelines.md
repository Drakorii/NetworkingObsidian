When choosing passwords, use strong passwords that are not easily guessed. There are some key points to consider when choosing passwords:

-   Use passwords that are more than eight characters in length.
-   Use a combination of upper and lowercase letters, numbers, special characters, and/or numeric sequences.
-   Avoid using the same password for all devices.
-   Do not use common words because they are easily guessed.

In a classroom environment always choose a very easy password (like cisco and class) or write it down! Otherwise you have to reset and start over.

To configure a password for user EXEC mode:
Sw-Floor-1# **configure terminal**
Sw-Floor-1(config)# **line console 0**
Sw-Floor-1(config-line)# **password cisco**
Sw-Floor-1(config-line)# **login**
Sw-Floor-1(config-line)# **end**
Sw-Floor-1#

To configure a password for user priviledged EXEC mode:
Sw-Floor-1# **configure terminal**
Sw-Floor-1(config)# **enable secret class**
Sw-Floor-1(config)# **exit**
Sw-Floor-1#

Many cisco switches support 16 vty lines for remote access via telnet or ssh. The lines are numbered from 0 to 15. If you want to configure the same password for all of them:
Sw-Floor-1# **configure terminal**
Sw-Floor-1(config)# **line vty 0 15**
Sw-Floor-1(config-line)# **password cisco** 
Sw-Floor-1(config-line)# **login** 
Sw-Floor-1(config-line)# **end**
Sw-Floor-1#

# Password Encryption

he startup-config and running-config files display most passwords in plaintext. This is a security threat because anyone can discover the passwords if they have access to these files.

To encrypt all plaintext passwords, use the **service password-encryption** global config command as shown in the example.

Sw-Floor-1# **configure terminal**
Sw-Floor-1(config)# **service password-encryption**
Sw-Floor-1(config)#
