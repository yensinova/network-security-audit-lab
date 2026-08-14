   # Fase 2: Reconocimiento y Descubrimiento de Activos

   ## 1. Metodología
   Se realizó un mapeo de la red aislada `10.99.99.0/24` utilizando técnicas de descubrimiento en Capa 2 (ARP) y Capa 3 (ICMP) para identificar la superficie de ataque inicial sin generar tráfico de escaneo de puertos prematuro.
   Todo el tráfico de red fue capturado mediante `tcpdump` para su posterior análisis forense y validación de las herramientas utilizadas.

   ## 2. Activos Identificados (Asset Inventory)

   | IP | MAC Address | Vendor (Fabricante) | Rol en el Laboratorio | Estado |
   |---|---|---|---|---|
   | 10.99.99.10 | 00:0c:29:xx:xx:xx | VMware | Máquina Atacante (Kali) | Activo |
   | 10.99.99.20 | 00:0c:29:yy:yy:yy | VMware | Objetivo (Metasploitable 2) | Activo |

   ## 3. Evidencias
   * [Captura de tráfico (PCAP)](../evidence/pcap/02-day2-discovery.pcap)
   * [Resultados Nmap (XML/NMAP)](../evidence/nmap/)
   * [Análisis Wireshark (Screenshots)](../evidence/screenshots/)