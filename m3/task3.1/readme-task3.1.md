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