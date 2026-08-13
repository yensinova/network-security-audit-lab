\## Evidencias de configuración



\### Red aislada VMnet2



VMnet2 se configuró como una red Host-only para mantener el laboratorio aislado del equipo anfitrión, la red local e Internet.


![Configuración Host-only de VMnet2](../evidence/setup/01-vmnet2-host-only.png)


\### Adaptador de Kali Linux



La máquina auditora Kali Linux se conectó a la red virtual VMnet2.



![Adaptador de Kali conectado a VMnet2](../evidence/setup/02-kali-adaptador-vmnet2.png)



\### Adaptador de Metasploitable 2



La máquina objetivo Metasploitable 2 se conectó exclusivamente a la misma red virtual VMnet2.



![Adaptador de Metasploitable conectado a VMnet2](../evidence/setup/03-metasploitable-adaptador-vmnet2.png)



\### Direccionamiento IP estático



Kali Linux utiliza la dirección `10.99.99.10/24` y Metasploitable 2 utiliza `10.99.99.20/24`.



![Dirección IP estática de Kali](../evidence/setup/04-kali-ip-estatica.png)



![Dirección IP estática de Metasploitable](../evidence/setup/05-metasploitable-ip-estatica.png)



\### Validación de conectividad



La conectividad desde Kali Linux hacia la máquina objetivo fue validada mediante ICMP.



![Ping desde Kali hacia Metasploitable](../evidence/setup/06-ping-kali-a-metasploitable.png)

