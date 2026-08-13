# \# Network Security Audit Lab

# 

# Laboratorio práctico y autorizado de auditoría de seguridad en una red virtual aislada.

# 

# \## Objetivo

# 

# Practicar las fases iniciales de una auditoría de red:

# 

# \- Definición de alcance y reglas de enfrentamiento

# \- Descubrimiento y enumeración de servicios

# \- Identificación y validación controlada de vulnerabilidades

# \- Documentación de evidencias y elaboración de informes

# 

# \## Entorno

# 

# | Elemento | Configuración |

# |---|---|

# | Máquina auditora | Kali Linux |

# | Máquina objetivo | Metasploitable 2 |

# | Red de laboratorio | 10.99.99.0/24 |

# | Kali | 10.99.99.10 |

# | Metasploitable 2 | 10.99.99.20 |

# | Virtualización | VMware Workstation |

# | Aislamiento | VMnet2 (Host-only) |

# 

# \## Estructura

# 

# \- `docs/`: Alcance, RoE y documentación del laboratorio

# \- `evidence/nmap/`: Resultados de escaneos Nmap

# \- `evidence/pcap/`: Capturas de tráfico autorizadas

# \- `reports/`: Informes técnicos y ejecutivos

# \- `scripts/`: Scripts propios usados en el laboratorio

# 

# \## Seguridad y autorización

# 

# Este repositorio documenta únicamente actividades realizadas en un entorno controlado y autorizado. No se realizan pruebas contra infraestructura externa, redes reales ni sistemas de terceros.

# 

# Consulta \[las reglas de enfrentamiento](docs/01-alcance-y-reglas.md) antes de continuar.

