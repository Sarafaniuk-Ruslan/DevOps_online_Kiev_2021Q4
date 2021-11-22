//Hello there

Very interesting situation 'cause I have been having access to Packet Traser. I am studying on a computer engineering course and we had lectures + practice with .... It was very interesting in practice to create a grid and customize it from 0. 

Made separate grids:

1.  Interprise - 10.1.30.0/24
2.  Data Center - 11.30.1.0/24
3.  Home office - 192.168.0.0/24

IP clients PC:

1PC.    192.168.0.40
2PC.   10.1.30.10 
3PC.   10.1.30.20

Servers IP:

Web server 01.  11.30.1.50
Web server 01.  11.30.1.100
DNS server.     11.30.1.150  /  DNS-4.25.99.150
DHCP server.    10.1.30.100


Download porgramm Wireshark and catch traffic of my rdp access.

MAC-address src: 2c:c8:1b:26:57:68
MAC-address dst: f0:2f:74:2e:7b:fc
IP-address src: 176.106.2.25
IP-address dst: 192.168.80.101
TCP-port src: 57451
TCP-port dst: 3389


Task 3.2

First of all, I did upgrate by adding new ethernet port for routing. Then, I did insidness grid.

ISP1:
- GE1/0
- GE2/0

ISP2:
- GE1/0
- GE3/0

ISP3:
- GE2/0
- GE3/0

New information for me was, adding and setting VLAN interface but actually it has not been difficult. I was setting all config by 20 minutes at all.

VLAN Number: 2
VLAN Name: WS1

VLAN Number: 3
VLAN Name: WS2

VLAN Number: 4
VLAN Name: WS3

I changed conf in first FE port from access to trunk mode which supports VLAN specifications. After that, I did this changes on router ISP3

Router(config)# interface GigabitEthernet0/0.2
Router(config-subif)#encapsulation dot1Q 2
Router(config-subif)#ip address 11.30.1.1 255.255.255.192

Router(config)# interface GigabitEthernet0/0.3
Router(config-subif)#encapsulation dot1Q 3
Router(config-subif)#ip address 11.30.1.65 255.255.255.192

Router(config)# interface GigabitEthernet0/0.4
Router(config-subif)#encapsulation dot1Q 4
Router(config-subif)#ip address 11.30.1.129 255.255.255.192
