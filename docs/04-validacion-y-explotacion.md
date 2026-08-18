\# Fase 4: Validación Controlada y Explotación



\## 1. Metodología

Se validaron los hallazgos identificados en la Fase 3 mediante confirmación manual

(banner grabbing y scripts NSE específicos) y explotación controlada en laboratorio

aislado. No se instalaron persistencias ni se modificaron configuraciones.



\## 2. Hallazgos Validados



| ID | Servicio | Vulnerabilidad | CVE | Validación | Impacto | Riesgo |

|----|----------|----------------|-----|------------|---------|--------|

| VUL-01 | FTP (vsftpd 2.3.4) | Backdoor en versión 2.3.4 | CVE-2011-2511 | Manual + NSE | Acceso root remoto | Crítico |

| VUL-02 | SMB (Samba 3.0.20) | Ejecución remota por username map script | CVE-2007-2447 | Metasploit | Acceso root remoto | Crítico |



\## 3. Evidencias

\* [Figura 6: Nmap NSE ftp-vsftpd-backdoor – VULNERABLE, CVE-2011-2523 (State: Exploitable)](../evidence/screenshots/06-nmap-vsftpd-backdoor-check.png)

\* [Figura 7: Explotación manual vsftpd 2.3.4 – trigger ":)" y shell root en puerto 6200 (id, whoami, uname -a)](../evidence/screenshots/07-vsftpd-manual-root.png)

\* [Figura 8: Metasploit exploit/multi/samba/usermap\_script – sesión command shell como root](../evidence/screenshots/08-samba-metasploit-root.png)

\* [Figura 9: Verificación post-remediación – puerto 21 abierto (servicio base) y 6200 Connection refused (backdoor eliminada)](../evidence/screenshots/09-post-remediacion-6200-cerrado.png)



\## 4. Análisis de Impacto (Enfoque IAM)

Ambos hallazgos permiten obtener acceso con privilegios `root`, lo que implica:

\- Compromiso total de identidades locales (`/etc/passwd`, `/etc/shadow`).

\- Acceso sin control a recursos compartidos SMB/NFS.

\- Incumplimiento del principio de mínimo privilegio.

\- Riesgo de movimiento lateral si el equipo estuviera conectado a otros segmentos.



\## 5. Remediación

| ID | Acción | Prioridad |

|----|--------|-----------|

| REC-01 | Actualizar vsftpd a versión soportada | Crítica |

| REC-02 | Actualizar Samba y deshabilitar `username map script` | Crítica |

| REC-03 | Segmentar servicios expuestos y filtrar puertos en firewall | Alta |

| REC-04 | Aplicar mínimo privilegio en cuentas de servicio y recursos compartidos | Alta |

| REC-05 | Monitorizar intentos de acceso anómalos (IDS/SIEM) | Media |

