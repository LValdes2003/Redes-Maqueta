```
enable
config terminal
hostname Rec-Switch
line console 0
password leonardo
login
exec-timeout 3 0
logging synchronous
exit
enable password leonardo
banner motd &Switch de recepción&
no ip domain-lookup
service password-encryption
username valdes password leonardo
ip domain-name leo.com
crypto key generate rsa general-keys modulus 1024
ip ssh version 2
line vty 0 15
login local
transport input ssh
exit
access-list 1 permit 192.168.10.0 0.0.0.255
access-list 1 deny any
line vty 0 15
access-class 1 in
exit
do write
hostname Rec-Switch
line console 0
password leonardo
login
exec-timeout 3 0
logging synchronous
exit
enable password leonardo
banner motd &Switch de recepción&
no ip domain-lookup
service password-encryption
username valdes password leonardo
ip domain-name leo.com
crypto key generate rsa general-keys modulus 1024
ip ssh version 2
line vty 0 15
login local
transport input ssh
exit
access-list 1 permit 192.168.10.0 0.0.0.255
access-list 1 deny any
line vty 0 15
access-class 1 in
exit
do write
```
