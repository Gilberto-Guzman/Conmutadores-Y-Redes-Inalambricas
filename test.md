Router(config)#interface f0/0
Router(config-if)#ip add 192.168.7.1 255.255.248.0
Router(config-if)#exit
Router(config)#ip dhcp pool RED_LAN2
Router(dhcp-config)#default-router 192.168.7.1
Router(dhcp-config)#dns-server 192.168.7.1
Router(dhcp-config)#network 192.168.7.1 255.255.248.0
Router(dhcp-config)#exit
Router(config)#ip dhcp excluded-address 192.168.7.1 192.168.7.21
Router(config)#exit
Router#
%SYS-5-CONFIG_I: Configured from console by console

Router(config)#interface f0/1
Router(config-if)#ip add 192.168.8.1 255.255.248.0
Router(config-if)#exit
Router(config)#ip dhcp pool RED_LAN2
Router(dhcp-config)#default-router 192.168.8.1
Router(dhcp-config)#dns-server 192.168.8.1
Router(dhcp-config)#network 192.168.8.1 255.255.248.0
Router(dhcp-config)#exit
Router(config)#ip dhcp excluded-address 192.168.8.1 192.168.8.21
Router(config)#exit
Router#
%SYS-5-CONFIG_I: Configured from console by console

