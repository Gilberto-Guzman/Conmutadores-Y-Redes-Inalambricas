Simulación de una red VLAN con dos switches cisco y ocho computadoras para mostrar la configuración básica. 

Las VLANs se hacen redes lógicas separadas sería posible utilizar la misma red y tener dos computadoras con la misma dirección IP, por ejemplo: si la IP 172.16.1.8 pertenece a dos VLAN separadas, no tendríamos conflictos de IP.

Sin embargo, aunque es posible no es recomendable pues se dificulta la administración de las redes, en este ejercicio se utilizan las siguientes VLANs.

172.16.1.0/24 vlan elige el numero
172.16.2.0/24 vlan eligen el numero
En los dos switches se configura la interfaz 24 en modo trunk para permitir que las computadoras conectadas a cada VLAN se puedan comunicar.

Los comandos utilizados son:

Para crear una VLAN, por ejemplo la VLAN "SISTEMAS" 

vlan 2
name SISTEMAS
exit

Para asignar una interfaz 0/1 a la VLAN "SISTEMAS"

interface fastEthernet 0/1
switchport access vlan 2
exit

Para poner la interfaz 24 en modo trunk

interface fastEthernet 0/24
switchport mode trunk 
exit