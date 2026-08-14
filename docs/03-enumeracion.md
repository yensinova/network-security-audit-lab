&#x20;  # Fase 3: Enumeración de Servicios y Detección de Vulnerabilidades



&#x20;  ## 1. Metodología

&#x20;  Se realizó un escaneo exhaustivo de puertos TCP (`-p-`) seguido de detección de versiones (`-sV`) y ejecución de scripts de vulnerabilidades (`--script vuln`) para identificar la superficie de ataque del activo `10.99.99.20`.



&#x20;  ## 2. Matriz de Servicios Identificados



&#x20;  | Puerto | Protocolo | Servicio | Versión | Estado | Notas |

&#x20;  |---|---|---|---|---|---|

&#x20;  | 21 | TCP | FTP | vsftpd 2.3.4 | Abierto | Posible backdoor |

&#x20;  | 22 | TCP | SSH | OpenSSH 4.7p1 | Abierto | Versión antigua |

&#x20;  | 80 | TCP | HTTP | Apache 2.2.8 | Abierto | Servidor web |

&#x20;  | 139/445 | TCP | SMB | Samba 3.0.20 | Abierto | Enumeración de usuarios activa |

&#x20;  | 2049 | TCP | NFS | - | Abierto | Recursos compartidos expuestos |



&#x20;  ## 3. Hallazgos Preliminares (NSE Scripts)



&#x20;  | ID | Servicio | CVE / Vulnerabilidad | Descripción | Riesgo |

&#x20;  |---|---|---|---|---|

&#x20;  | VUL-01 | FTP | CVE-2011-2511 | vsftpd 2.3.4 Backdoor | Crítico |

&#x20;  | VUL-02 | SMB | CVE-2007-2447 | Samba "username map script" | Crítico |

&#x20;  | VUL-03 | NFS | - | Exposición de directorios raíz | Alto |



&#x20;  ## 4. Evidencias

&#x20;  \* \[Escaneo Completo TCP](../evidence/nmap/03-full-tcp.nmap)

&#x20;  \* \[Escaneo de Versiones y Scripts Default](../evidence/nmap/04-service-version.nmap)

&#x20;  \* \[Escaneo de Vulnerabilidades NSE](../evidence/nmap/05-vuln-scan.nmap)

