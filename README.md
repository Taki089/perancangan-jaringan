Perancangan Jaringan Lab Amikom.

Proyek ini bertujuan untuk merancang jaringan komputer yang efisien dan dapat
diandalkan untuk digunakan di laboratorium komputer di Universitas AMIKOM. Lab
ini akan digunakan untuk keperluan akademik dan penelitian oleh mahasiswa dan
staf pengajar. Universitas AMIKOM dikenal sebagai salah satu institusi pendidikan
terkemuka di bidang teknologi informasi dan komputer di Indonesia. Proyek ini
terdapat 10 lab komputer dengan masing-masing berjumlah 40 komputer dan
terdapat 20 orang staff IT.

![Screenshot 2024-11-08 130214](https://github.com/user-attachments/assets/c6c874ca-4a76-4da6-b2a2-d08e7a90eea1)


![Screenshot 2024-11-08 130401](https://github.com/user-attachments/assets/b558fd47-8746-4e7f-b43d-ae84a9c87289)

1. Alokasi IP Network
IP Network dan Prefix VLAN ID Divisi / Tempat
192.168.1.0/24 - Router 1 - MLS 1
192.168.2.0/24 - Router 1 - MLS 2
1.1.1.0/24 - Router 1 - EDGE ROUTER
192.168.3.0/24 - Router 2 - MLS 2
192.168.4.0/24 - Router 2 - MLS 1
1.1.2.0/24 - Router 2 -EDGE ROUTER
172.16.10.0/24 VLAN 10 Server
172.16.21.0/24 VLAN 21 PC Lab 1
172.16.22.0/24 VLAN 22 PC Lab 2
172.16.23.0/24 VLAN 23 PC Lab 3
172.16.24.0/24 VLAN 24 PC Lab 4
172.16.25.0/24 VLAN 25 PC UPT
172.16.26.0/24 VLAN 26 PC Lab 9
172.16.27.0/24 VLAN 27 PC Lab 10
172.16.28.0/24 VLAN 28 PC Lab 8
172.16.29.0/24 VLAN 29 PC Lab 7
172.16.30.0/24 VLAN 30 PC Lab 6
172.16.31.0/24 VLAN 31 PC Lab 5
172.16.99.0/24 VLAN 99 Management
172.16.42.0/24 VLAN 42 APUPT
172.16.43.0/24 VLAN 43 APL3
172.16.44.0/24 VLAN 44 APL4
172.16.45.0/24 VLAN 45 APL5
172.16.46.0/24 VLAN 46 APL6n 
172.16.47.0/24 VLAN 47 APL7

2. Alokasi IP Host
Jenis Perangkat Nama Perangkat Interface IP Address Subnet Mask
Router Router 1 Gig0/0 1.1.1.1/24 255.255.255.0
Router Router 1 Gig0/1 192.168.1.1/24 255.255.255.0
Router Router 1 Gig0/2 192.168.2.1/24 255.255.255.0
Router Router 2 Gig0/0 1.1.2.1/24 255.255.255.0
Router Router 2 Gig0/1 192.168.3.1/24 255.255.255.0
Router Router 2 Gig0/2 192.168.4.1/24 255.255.255.0
Multilayer Switch MLS 1 Gig0/1 192.168.1.2/24 255.255.255.0
Multilayer Switch MSL 1 Gig0/2 192.168.4.2/24 255.255.255.0
Multilayer Switch MLS 2 Gig0/1 192.168.3.2/24 255.255.255.0
Multilayer Switch MLS 2 Gig0/2 192.168.2.2/24 255.255.255.0
Server Web Server 172.16.10.2 255.255.255.0
Server DNS Server 172.16.10.3 255.255.255.0
Server File Server 172.16.10.4 255.255.255.0
PC PC Lab 1 172.16.21.2-253 255.255.255.0
PC PC Lab 2 172.16.22.2-253 255.255.255.0
PC PC Lab 3 172.16.23.2-253 255.255.255.0
PC PC Lab 4 172.16.24.2-253 255.255.255.0
PC PC UPT 172.16.25.2-7 255.255.255.0
PC PC Lab 9 172.16.26.2-253 255.255.255.0
PC PC Lab 10 172.16.27.2-253 255.255.255.0
PC PC Lab 8 172.16.28.2-253 255.255.255.0
PC PC Lab 7 172.16.29.2-253 255.255.255.0
PC PC Lab 6 172.16.30.2-253 255.255.255.0
PC PC Lab 5 172.16.31.2-253 255.255.255.0
Access Point AP 172.16.42.1-253 255.255.255.0
Access Point APL3 172.16.43.1-253 255.255.255.0
Access Point APL4 172.16.44.1-253 255.255.255.0
Access Point APL5 172.16.45.1-253 255.255.255.0
Access Point APL6 172.16.46.1-253 255.255.255.0
Access Point APL7 172.16.47.1-253 255.255.255.0

Tahapan konfigurasi pada Router Publik (R-PUBLIC) yaitu:
1. Hostname
Hostname Router EDGE
2. Setting Routing
Router(config)#ip route 172.16.10.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.21.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.22.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.23.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.24.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.25.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.26.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.27.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.28.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.29.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.30.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.31.0 255.255.255.0 1.1.1.1
Router(config)#ip route 172.16.10.0 255.255.255.0 1.1.2.1
Router(config)#ip route 172.16.21.0 255.255.255.0 1.1.2.1
Router(config)#ip route 172.16.22.0 255.255.255.0 1.1.2.1
Router(config)#ip route 172.16.23.0 255.255.255.0 1.1.2.1
Router(config)#ip route 172.16.24.0 255.255.255.0 1.1.2.1
Router(config)#ip route 172.16.25.0 255.255.255.0 1.1.2.1
Router(config)#ip route 172.16.26.0 255.255.255.0 1.1.2.1
Router(config)#ip route 172.16.27.0 255.255.255.0 1.1.2.1
Router(config)#ip route 172.16.28.0 255.255.255.0 1.1.2.1
Router(config)#ip route 172.16.29.0 255.255.255.0 1.1.2.1
Router(config)#ip route 172.16.30.0 255.255.255.0 1.1.2.1
Router(config)#ip route 172.16.31.0 255.255.255.0 1.1.2.1
Router(config)#interface GigabitEthernet0/2
Router(config-if)#no shutdown
Router(config-if)#ip address 8.8.8.1 255.0.0.0
Router(config-if)#ip address 8.8.8.1 255.255.255.0

4. Setting NAT
Router(config-if)#int gig0/0
Router(config-if)#ip nat outside
Router(config-if)#int gig0/1
Router(config-if)#ip nat inside
Router(config-if)#int gig0/2
Router(config-if)#ip nat outside
Router(config-if)#ex

B. Router
1. Hostname dan IP Address
hostname R1 / R2
interface GigabitEthernet0/0
ip address 1.1.1.1 255.255.255.0
interface GigabitEthernet0/1
ip address 192.168.1.1 255.255.255.0
interface GigabitEthernet0/2
ip address 192.168.2.1 255.255.255.0

2. Routing
router ospf 1
network 1.1.1.0 0.0.0.255 area 0
network 192.168.1.0 0.0.0.255 area 0
network 192.168.2.0 0.0.0.255 area 0

Tahapan konfigurasi pada SW-Core1
yaitu:

1. Hostname dan IP address
Switch#en
Switch#hostname MLS1
interface GigabitEthernet0/1
no switchport

ip address 192.168.1.2 255.255.255.0
interface GigabitEthernet0/2
no switchport

ip address 192.168.4.2 255.255.255.0
interface Vlan10
ip address 172.16.10.1 255.255.255.0
interface Vlan21
ip address 172.16.21.1 255.255.255.0
interface Vlan22
ip address 172.16.22.1 255.255.255.0
interface Vlan23
ip address 172.16.23.1 255.255.255.0
interface Vlan24
ip address 172.16.24.1 255.255.255.0
interface Vlan25
ip address 172.16.25.1 255.255.255.0
interface Vlan26
ip address 172.16.26.1 255.255.255.0
interface Vlan27
ip address 172.16.27.1 255.255.255.0
interface Vlan28
ip address 172.16.28.1 255.255.255.0
interface Vlan29
ip address 172.16.29.1 255.255.255.0
interface Vlan30
ip address 172.16.30.1 255.255.255.0
interface Vlan31
ip address 172.16.31.1 255.255.255.0
interface Vlan42
ip address 172.16.42.254 255.255.255.0
interface Vlan43
ip address 172.16.43.254 255.255.255.0
interface Vlan44
ip address 172.16.44.254 255.255.255.0
interface Vlan45
ip address 172.16.45.254 255.255.255.0
interface Vlan46
ip address 172.16.46.254 255.255.255.0
interface Vlan47
ip address 172.16.47.254 255.255.255.0
interface Vlan99
ip address 172.16.99.3 255.255.255.0

2. VLAN, dst.
MLS1
Switch#en
Switch#hostname MLS1
MLS1(config)#int fa0/3
MLS1(config-if)#switchport trunk encapsulation dot1q
MLS1(config-if)#switchport mode trunk
MLS1(config-if)#ip routing
MLS1(config)#int vlan 23
MLS1(config-if)#ip address 172.16.23.1 255.255.255.0
MLS1(config-if)#no sh
MLS1(config-if)#int vlan 24
MLS1(config-if)#ip address 172.16.24.1 255.255.255.0
MLS1(config-if)#no sh
MLS1(config-if)#int fa0/5
MLS1(config-if)#switchport trunk encapsulation dot1q
MLS1(config-if)#switchport mode trunk
MLS1(config-if)#int vlan 25
MLS1(config-if)#ip address 172.16.25.1 255.255.255.0
MLS1(config-if)#no sh
MLS1(config)#int vlan 26
MLS1(config-if)#ip address 172.16.26.1 255.255.255.0
MLS1(config-if)#no sh
MLS1(config-if)#int fa0/9
MLS1(config-if)#switchport trunk encapsulation dot1q
MLS1(config-if)#switchport mode trunk
MLS1(config-if)#int vlan 27
MLS1(config-if)#ip address 172.16.27.1 255.255.255.0
MLS1(config-if)#no sh
MLS1(config-if)#ex
MLS1(config)#int vlan 28
MLS1(config-if)#ip address 172.16.28.1 255.255.255.0
MLS1(config-if)#no sh
MLS1(config-if)#ex
MLS1(config)#int vlan 29
MLS1(config-if)#ip address 172.16.29.1 255.255.255.0
MLS1(config-if)#no sh
MLS1(config-if)#ex
MLS1(config)#int vlan 30
MLS1(config-if)#ip address 172.16.30.1 255.255.255.0
MLS1(config-if)#no sh
MLS1(config-if)#ex
MLS1#conf t
MLS1(config)#vlan 99
MLS1(config-vlan)#name VLAN_MANAGEMENT
MLS1(config-vlan)#ex
MLS1(config)#username PJ secret 123
MLS1(config)#line vty 0 15
MLS1(config-line)#password 123
MLS1(config-line)#login local
MLS1(config-line)#transport input telnet
MLS1(config-line)#exit
MLS1(config)#int vlan 99
MLS1(config-if)#ip add 172.16.99.3 255.255.255.0
MLS1(config)#enable password 123
MLS1(config)#ip dhcp pool v21
MLS1(dhcp-config)#default-router 172.16.21.1
MLS1(dhcp-config)#network 172.16.21.0 255.255.255.0
SWLantai3(config)#interface FastEthernet0/2
SWLantai3(config-if)#switchport access vlan 21
MLS1(dhcp-config)#ex
MLS1(config)#int vlan 42
MLS1(config-if)#description APUPT
MLS1(config-if)#ip address 172.16.42.254 255.255.255.0
MLS1(config-if)#ex
MLS1(config)#int vlan 43
MLS1(config-if)#description APL3
MLS1(config-if)#ip address 172.16.43.254 255.255.255.0
MLS1(config-if)#ex
MLS1(config)#int vlan 44
MLS1(config-if)#desc APL4
MLS1(config-if)#ip address 172.16.44.254 255.255.255.0
MLS1(config-if)#ex
MLS1(config)#int vlan 45
MLS1(config-if)#desc APL5
MLS1(config-if)#ip address 172.16.45.254 255.255.255.0
MLS1(config-if)#ex
MLS1(config)#int vlan 46
MLS1(config-if)#desc APL6
MLS1(config-if)#ip address 172.16.46.254 255.255.255.0
MLS1(config-if)#ex
MLS1(config)#int vlan 47
MLS1(config-if)#desc APL7
MLS1(config-if)#ip address 172.16.47.254 255.255.255.0
MLS1(config-if)#ex
MLS1(config)#ip dhcp pool APUPT
MLS1(dhcp-config)#network 172.16.43.0 255.255.255.0
MLS1(dhcp-config)#default-router 172.16.42.1
MLS1(dhcp-config)#network 172.16.42.0 255.255.255.0
MLS1(config-if)#ip address 172.16.47.254 255.255.255.0
MLS1(dhcp-config)#ex
MLS1(config)#ip dhcp pool APL3
MLS1(dhcp-config)#default-router 172.16.43.254
MLS1(dhcp-config)#network 172.16.43.0 255.255.255.0
MLS1(dhcp-config)#ex
MLS1(config)#ip dhcp pool APUPT
MLS1(dhcp-config)#default-router 172.16.42.254
MLS1(dhcp-config)#ex
MLS1(config)#ip dhcp pool APL4
MLS1(dhcp-config)#default-router 172.16.44.254
MLS1(dhcp-config)#network 172.16.44.0 255.255.255.0
MLS1(dhcp-config)#ex
MLS1(config)#ip dhcp pool APL5
MLS1(dhcp-config)#network 172.16.45.254
MLS1(dhcp-config)#network 172.16.45.0 255.255.255.0
MLS1(dhcp-config)#default-router 172.16.45.254
MLS1(dhcp-config)#ex
MLS1(config)#ip dhcp pool APL6
MLS1(dhcp-config)#default-router 172.16.46.254
MLS1(dhcp-config)#network 172.16.46.0 255.255.255.0
MLS1(dhcp-config)#ex
MLS1(config)#ip dhcp pool APL7
MLS1(dhcp-config)#default-router 172.16.47.254
MLS1(dhcp-config)#network 172.16.47.0 255.255.255.0

MLS2
Switch#en
Switch#hostname MLS2
MLS2(config)#vlan 21
MLS2(config-vlan)#name Lab1
MLS2(config-vlan)#vlan 22
MLS2(config-vlan)#name Lab2
MLS2(config-vlan)#vlan 23
MLS2(config-vlan)#name Lab3
MLS2(config-vlan)#vlan 24
MLS2(config-vlan)#name Lab4
MLS2(config-vlan)#vlan 25
MLS2(config-vlan)#name UPT
MLS2(config-vlan)#vlan 26
MLS2(config-vlan)#name Lab9
MLS2(config-vlan)#vlan 27
MLS2(config-vlan)#name Lab10
MLS2(config-vlan)#vlan 28
MLS2(config-vlan)#name Lab8
MLS2(config-vlan)#vlan 29
MLS2(config-vlan)#name Lab7
MLS2(config-vlan)#vlan 30
MLS2(config-vlan)#name Lab6
MLS2(config-vlan)#vlan 31
MLS2(config-vlan)#name Lab5
MLS2(config-vlan)#vlan 201
MLS2(config-vlan)#name SWL3
MLS2(config-vlan)#vlan 202
MLS2(config-vlan)#name SWL4
MLS2(config-vlan)#vlan 203
MLS2(config-vlan)#name SWUPT
MLS2(config-vlan)#vlan 204
MLS2(config-vlan)#name SWL7
MLS2(config-vlan)#vlan 205
MLS2(config-vlan)#name SWL6
MLS2(config-vlan)#ex
MLS2(config)#int fa0/5
MLS2(config-if)#switchport trunk encapsulation dot1q
MLS2(config-if)#switchport mode trunk
MLS2(config-if)#ip routing
MLS2(config)#int vlan 26
MLS2(config-if)#ip address 172.16.26.254 255.255.255.0
MLS2(config-if)#no sh
MLS2(config-if)#int vlan 27
MLS2(config-if)#ip address 172.16.27.254 255.255.255.0
MLS2(config-if)#no sh
MLS2(config-if)#ex
MLS2(config)#int fa0/9
MLS2(config-if)#switchport trunk encapsulation dot1q
MLS2(config-if)#switchport mode trunk
MLS2(config-if)#int vlan 21
MLS2(config-if)#ip address 172.16.21.254 255.255.255.0
MLS2(config-if)#no sh
MLS2(config-if)#int vlan 22
MLS2(config-if)#ip address 172.16.22.254 255.255.255.0
MLS2(config-if)#no sh
MLS2(config-if)#ex
MLS2(config)#int vlan 23
MLS2(config-if)#ip address 172.16.23.254 255.255.255.0
MLS2(config-if)#no sh
MLS2(config-if)#int vlan 24
MLS2(config-if)#ip address 172.16.24.254 255.255.255.0
MLS2(config-if)#no sh
MLS2(config-if)#int vlan 25
MLS2(config-if)#ip address 172.16.25.254 255.255.255.0
MLS2(config-if)#no sh
MLS2(config-if)#int vlan 27
MLS2(config-if)#exc
MLS2(config-if)#int vlan 28
MLS2(config-if)#ip address 172.16.28.254 255.255.255.0
MLS2(config-if)#no sh
MLS2(config-if)#int vlan 29
MLS2(config-if)#ip address 172.16.29.254 255.255.255.0
MLS2(config-if)#no sh
MLS2(config-if)#int vlan 30
MLS2(config-if)#ip address 172.16.30.254 255.255.255.0
MLS2(config-if)#no sh
MLS2(config-if)#int fa0/3
MLS2(config)#ip routing
MLS2(config)#vlan 10
MLS2(config-vlan)#name SERVER_VLAN
MLS2(config)#int fa0/6
MLS2(config-if)#switchport mode access
MLS2(config-if)#switchport access vlan 10
MLS2(config-if)#int fa0/7
MLS2(config-if)#switchport mode access
MLS2(config-if)#switchport access vlan 10
MLS2(config-if)#int fa0/8
MLS2(config-if)#switchport mode access
MLS2(config-if)#switchport access vlan 10
MLS2(config-if)#ex
MLS2(config)#int vlan 10
MLS2(config)#ip address 172.16.10.1 255.255.255.0
MLS2(config)#vlan 99
MLS2(config-vlan)#name VLAN_MANAGEMENT
MLS2(config-vlan)#ex
MLS2(config)#username PJ secret 123
MLS2(config)#line vty 0 15
MLS2(config-line)#password 123
MLS2(config-line)#login local
MLS2(config-line)#transport input telnet
MLS2(config-line)#exit
MLS2(config)#int vlan 99
MLS2(config-if)#ip add 172.16.99.5 255.255.255.0
MLS2(config)#enable password 123

Tahapan konfigurasi pada Switch Lab
yaitu:

Switch>en
Switch#conft
Switch(config)#vlan 21
Switch(config-vlan)#vlan 22
Switch(config-vlan)#name Lab2
Switch(config-vlan)#vlan 23
Switch(config-vlan)#name Lab3
Switch(config-vlan)#vlan 24
Switch(config-vlan)#name Lab4
Switch(config-vlan)#vlan 25
Switch(config-vlan)#name UT
Switch(config-vlan)#vlan 26
Switch(config-vlan)#name Lab9
Switch(config-vlan)#vlan 27
Switch(config-vlan)#name Lab10
Switch(config-vlan)#vlan 28
Switch(config-vlan)#name Lab8
Switch(config-vlan)#vlan 29
Switch(config-vlan)#name Lab7
Switch(config-vlan)#vlan 30
Switch(config-vlan)#name Lab6
Switch(config-vlan)#vlan 31
Switch(config-vlan)#name Lab5
Switch(config-vlan)#vlan 201
Switch(config-vlan)#name SWL3
Switch(config-vlan)#vlan 202
Switch(config-vlan)#name SWL4
Switch(config-vlan)#vlan 203
Switch(config-vlan)#name SWUPT
Switch(config-vlan)#vlan 204
Switch(config-vlan)#name SWL7
Switch(config-vlan)#vlan 205
Switch(config-vlan)#name SWL6
Switch(config-vlan)#vlan 206
Switch(config-vlan)#name SWL5
Switch(config-vlan)#ex
Switch(config)#int fa0/3
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 21
Switch(config-if)#ex
Switch(config)#int fa0/2
Switch(config-if)#int fa0/1
Switch(config-if)#switchport mode trunk
Switch(config-if)#vlan 99
Switch(config-vlan)#name VLAN_MANAGEMENT
Switch(config-vlan)#ex
Switch(config)#line vty0 15 
Switch(config-line)#password 123 
Switch(config-line)#login local 
Switch(config-line)#transport input telnet 
Switch(config-line)#exit 
Switch(config)#enable password 123
Switch(config)#int vlan 99 
Switch(config-if)#ip add 172.16.99.4 255.255.255.0 
