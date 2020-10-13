# TOPOLOGIA
![image](https://user-images.githubusercontent.com/20384738/95910579-85a16a80-0d5d-11eb-8426-6a0e9ce277d3.png)

# ROUTER VLAN
![image](https://user-images.githubusercontent.com/20384738/95909752-40306d80-0d5c-11eb-8690-fe6c451b3075.png)

Creamos la configuración llama Router On-a-Stick que nos permite tener subinterfaces y configurar estas a las VLANS
## COMANDOS
    - Encapsulation dot1q 10: Configuramos la subinterfaz a la VLAN 10
    - no shutdown: Levantamos la interfaz fisica

# SW1 VLAN
![image](https://user-images.githubusercontent.com/20384738/95909849-63f3b380-0d5c-11eb-9866-3e989532b89e.png)

Configuramos el SW1 como el gestor de las VLANS
## COMANDOS
    - vtp domain: El nombre que tendrá nuestro dominio
    - vtp password: La contraseña de nuestro dominio
    - vtp v2-mode:  El modo de la vlan
    - vtp-Server: El switch se configura como servidor para los demás switch

# CREACION DE VLAN
![image](https://user-images.githubusercontent.com/20384738/95909909-808feb80-0d5c-11eb-8dac-93e8fa578abb.png)

Configuramos las VLAN
## COMANDOS
    - VENTAS: Vlan 10
    - CONTABILIDAD: VLAN 20

# SW2 VLAN
![image](https://user-images.githubusercontent.com/20384738/95909993-a0271400-0d5c-11eb-8588-939c7908f974.png)

Configuramos el dominio en el resto de los switch para que las vlan se repliquen
## COMANDOS
    - VTP CLIENT: El switch se configurar en modo cliente

# CONFIGURACIONES DE INTERFACES
![image](https://user-images.githubusercontent.com/20384738/95910156-dbc1de00-0d5c-11eb-9e10-9330597a3dd1.png)

Las interfaces se configuran en modo trunk

# PC1 
![image](https://user-images.githubusercontent.com/20384738/95910191-e8463680-0d5c-11eb-81d7-45df8ef626e6.png)

# PO1
![image](https://user-images.githubusercontent.com/20384738/95910265-09a72280-0d5d-11eb-91d0-8af835e588e9.png)

PortChannel 1 del SW1 al SW2, también se configura de manera trunk, speed 100 y duplex full

# PO2
![image](https://user-images.githubusercontent.com/20384738/95910292-17f53e80-0d5d-11eb-8e94-8a696608019e.png)

PortChannel 2 del SW1 al SW3, también se configura de manera trunk, speed 100 y duplex full

# PO3
![image](https://user-images.githubusercontent.com/20384738/95910322-23486a00-0d5d-11eb-8c9b-e8291759ecb2.png)

PortChannel 2 del SW2 al SW3, también se configura de manera trunk, speed 100 y duplex full

# PUERTOS BLOQUEADO
![image](https://user-images.githubusercontent.com/20384738/95910360-30655900-0d5d-11eb-90d7-9c1510603f2e.png)

![image](https://user-images.githubusercontent.com/20384738/95910374-34917680-0d5d-11eb-844f-2602c9c81b31.png)

Los puertos bloqueados los podemos observar con el comando sh spanning-tree

# ROOT-BRIDGED
![image](https://user-images.githubusercontent.com/20384738/95910430-4d019100-0d5d-11eb-8439-7544973e0fd0.png)

![image](https://user-images.githubusercontent.com/20384738/95910538-77ebe500-0d5d-11eb-854e-31338f6fd85c.png)

