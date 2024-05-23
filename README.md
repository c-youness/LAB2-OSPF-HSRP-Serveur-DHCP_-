![TOPOLOGIE](https://github.com/chalyouness/LAB2-OSPF-HSRP-Serveur-DHCP_-/assets/114768920/efaaa0ab-8ebf-4027-8bc4-af35906947a1)

![PARTIE 1](https://github.com/chalyouness/LAB2-OSPF-HSRP-Serveur-DHCP_-/assets/114768920/4d9e199e-d005-4b4e-ab90-5219524d072b)

![CONFIG_SERVER 1,2](https://github.com/chalyouness/LAB2-OSPF-HSRP-Serveur-DHCP_-/assets/114768920/7091a1ee-b70f-4300-a13e-9a82a5937dce)


![PARTIE 2](https://github.com/chalyouness/LAB2-OSPF-HSRP-Serveur-DHCP_-/assets/114768920/c197b39a-03e5-4370-8d91-1f7c15faa6b2)

![router_1](https://github.com/chalyouness/LAB2-OSPF-HSRP-Serveur-DHCP_-/assets/114768920/bda08980-a2f4-4d2b-bcee-54487e0259ae)


Router_1(config)#interface fastEthernet 0/0
==============
Router_1(config-if)# ip address 50.10.10.3 255.255.255.224
==============
Router_1(config-if)#no shutdown 
==============
Router_1(config)#interface FastEthernet0/1
==============
Router_1(config-if)# ip address 172.16.10.2 255.255.255.192
==============
Router_1(config-if)#no shutdown 
==============
Activation OSPF
============
Router_1(config)#router ospf 1
============
Router_1(config-router)#network 50.10.10.0 0.0.0.31 area 0
============
Router_1(config-router)#network 172.16.10.0 0.0.0.63 area 0
============


![router_2](https://github.com/chalyouness/LAB2-OSPF-HSRP-Serveur-DHCP_-/assets/114768920/9187a03b-34c0-49b6-bfb4-ffac9ab4c66c)

Router_2(config)#interface fastEthernet 0/0
==============
Router_2(config-if)# ip address 50.10.10.4 255.255.255.224
==============
Router_2(config-if)#no shutdown 
==============
Router_2(config)#interface FastEthernet0/1
==============
Router_2(config-if)# ip address 172.16.10.3 255.255.255.192
==============
Router_2(config-if)#no shutdown 
==============

Activation OSPF
============
Router_2(config)#router ospf 1
============
Router_2(config-router)#network 172.16.10.0 0.0.0.63 area 0
============
Router_2(config-router)#network 50.10.10.0 0.0.0.31 area 0
============

![router_3](https://github.com/chalyouness/LAB2-OSPF-HSRP-Serveur-DHCP_-/assets/114768920/3f8082ad-ec8f-4dea-900b-f3a315f7bc92)

Router_3(config)#interface fastEthernet 0/0
==============
Router_3(config-if)# ip address 10.10.10.2 255.255.255.0
==============
Router_3(config-if)#no shutdown 
============
Router_2(config)#interface fastEthernet 0/1
==============
Router_3(config-if)# ip address 50.10.10.1 255.255.255.224
==============
Router_3(config-if)#no shutdown 
============
Activation OSPF
============
Router_3(config)#router ospf 1
============
Router_3(config-router)#network 10.10.10.0 0.0.0.255 area 0
============
Router_3(config-router)#network 50.10.10.0 0.0.0.31 area 0
============
![router_4](https://github.com/chalyouness/LAB2-OSPF-HSRP-Serveur-DHCP_-/assets/114768920/bfc72583-da65-41b0-8cfe-ea0318893327)

Router_4(config)#interface fastEthernet 0/0
==============
Router_4(config-if)# ip address 10.10.10.3 255.255.255.0
==============
Router_4(config-if)#no shutdown 
============
Router_4(config)#interface fastEthernet 0/1
==============
Router_4(config-if)# ip address 50.10.10.2 255.255.255.224
==============
Router_4(config-if)#no shutdown 
============
Activation OSPF
============
Router_4(config)#router ospf 1
============
Router_4(config-router)#network 10.10.10.0 0.0.0.255 area 0
============
Router_4(config-router)#network 50.10.10.0 0.0.0.31 area 0
============
![router_DHCP-Server](https://github.com/chalyouness/LAB2-OSPF-HSRP-Serveur-DHCP_-/assets/114768920/41136a77-8863-4bb5-bd96-3804d9e69ac8)

C.Youness(DHCP-Server)(config)#hostname C.Youness(DHCP-Server)
==============
C.Youness(DHCP-Server)(config)#interface fastEthernet 0/0
==============
C.Youness(DHCP-Server)(config-if)#ip address 10.10.10.4 255.255.255.0 
==============

Activation DHCP Server
==============
C.Youness(DHCP-Server)(config)#ip dhcp pool C.Youness
==============
C.Youness(DHCP-Server)(dhcp-config)#network 10.10.10.0 255.255.255.0
==============
C.Youness(DHCP-Server)(dhcp-config)#default-router 10.10.10.1
==============
C.Youness(DHCP-Server)(dhcp-config)#dns-server 1.1.1.1
==============
C.Youness(DHCP-Server)(dhcp-config)#ip dhcp excluded-address 10.10.10.1
==============
C.Youness(DHCP-Server)(config)#ip dhcp excluded-address 10.10.10.2
==============
C.Youness(DHCP-Server)(config)#ip dhcp excluded-address 10.10.10.3
==============
C.Youness(DHCP-Server)(config)#ip dhcp excluded-address 10.10.10.4
==============


 ![PARTIE 3](https://github.com/chalyouness/LAB2-OSPF-HSRP-Serveur-DHCP_-/assets/114768920/e893e896-f5ab-47dd-8e52-44358d24603a)



