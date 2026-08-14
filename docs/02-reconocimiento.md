&#x20;  # Fase 2: Reconocimiento y Descubrimiento de Activos



&#x20;  ## 1. Metodología

&#x20;  Se realizó un mapeo de la red aislada `10.99.99.0/24` utilizando técnicas de descubrimiento en Capa 2 (ARP) y Capa 3 (ICMP) para identificar la superficie de ataque inicial sin generar tráfico de escaneo de puertos prematuro.

&#x20;  Todo el tráfico de red fue capturado mediante `tcpdump` para su posterior análisis forense y validación de las herramientas utilizadas.



&#x20;  ## 2. Activos Identificados (Asset Inventory)



&#x20;  | IP | MAC Address | Vendor (Fabricante) | Rol en el Laboratorio | Estado |

&#x20;  |---|---|---|---|---|

&#x20;  | 10.99.99.10 | 00:0c:29:xx:xx:xx | VMware | Máquina Atacante (Kali) | Activo |

&#x20;  | 10.99.99.20 | 00:0c:29:yy:yy:yy | VMware | Objetivo (Metasploitable 2) | Activo |



&#x20;  ## 3. Evidencias

&#x20;  \* \[Captura de tráfico (PCAP)](../evidence/pcap/02-day2-discovery.pcap)

&#x20;  \* \[Resultados Nmap (XML/NMAP)](../evidence/nmap/)

&#x20;  \* \[Análisis Wireshark (Screenshots)](../evidence/screenshots/)

&#x20;  \* [Figura 1: Wireshark, filtro "arp" – barrido ARP "Who has 10.99.99.x? Tell 10.99.99.10" desde Kali (10.99.99.10)](../evidence/screenshots/02-day2-wireshark-arp-sweep.png)
&#x20;  \* [Figura 2: Wireshark, filtro "icmp" – Echo (ping) reply de Metasploitable (10.99.99.20) hacia Kali (10.99.99.10)](../evidence/screenshots/03-day2-wireshark-icmp-reply.png)