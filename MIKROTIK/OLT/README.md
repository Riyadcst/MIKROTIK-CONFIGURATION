#enable
#config ter
#vlan 500 - 504
#exit


#interface gigbitethernet 0/1
#switchport mode trunk
#switchport trunk vlan 500 - 504
#description **UPLINK**
#speed 1000
#no shutdown
#exit


#interface vlan 500
#ip address 10.16.16.2 255.255.255.252
#exit


#ip route 0.0.0.0/0 10.16.16.1
#exit


#interface epon 0/1
#switchport mode access
#switchport access vlan 501
#exit


#no access telnet 0.0.0.0/0 192.168.8.1/24
 

