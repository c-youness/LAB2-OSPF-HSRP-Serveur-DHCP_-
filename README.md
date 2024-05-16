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

