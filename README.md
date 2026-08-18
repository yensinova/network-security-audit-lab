# 🛡️ Auditoría de Seguridad en Laboratorio de Red

Proyecto de pentesting ético realizado en un **laboratorio virtual aislado**,
aplicando una metodología completa de auditoría: reconocimiento, enumeración,
detección de vulnerabilidades, explotación controlada y reporting.

> ⚠️ **Aviso ético:** Este proyecto se realizó exclusivamente sobre máquinas
> virtuales locales y autorizadas. No se atacaron sistemas reales ni de terceros.

## 🎯 Objetivo

Identificar servicios expuestos, vulnerabilidades críticas y validar su
explotación de forma controlada, generando un informe técnico con
recomendaciones de remediación.

## 🧪 Entorno del Laboratorio

| Componente | Detalle |
|-----------|---------|
| Hipervisor | VMware Workstation |
| Atacante | Kali Linux |
| Objetivo | Metasploitable 2 |
| Red | Aislada (host-only) `10.99.99.0/24` |

## 🛠️ Herramientas Utilizadas

- **Nmap** — Descubrimiento, enumeración y NSE scripts
- **Wireshark / tcpdump** — Captura y análisis de tráfico (PCAP)
- **Metasploit Framework** — Explotación controlada
- **Netcat** — Validación manual de servicios
- **Pandoc** — Generación automatizada de informes PDF

## 📋 Metodología Aplicada

1. **Reconocimiento** — Descubrimiento de activos y captura de tráfico
2. **Enumeración** — Servicios, versiones y scripts NSE
3. **Detección de vulnerabilidades** — Identificación de CVEs
4. **Validación y explotación** — Confirmación controlada de hallazgos
5. **Reporting** — Informe técnico y remediación

## 🔍 Hallazgos Principales

| ID | Servicio | Vulnerabilidad | Severidad |
|----|----------|----------------|-----------|
| VUL-01 | FTP | Backdoor vsftpd 2.3.4 | 🔴 Crítica |
| VUL-02 | SMB | Samba usermap_script | 🔴 Crítica |

📄 **Informe completo:** [reports/informe-final.pdf](reports/informe-final.pdf)

## 📁 Estructura del Repositorio

- `docs/` — Documentación de alcance, metodología y hallazgos
- `evidence/` — Evidencias sanitizadas (Nmap, capturas, PCAP)
- `reports/` — Informe técnico final en PDF
- `scripts/` — Scripts de automatización

## 👤 Autor

**Yensi Jesús González Nova**
Soporte Técnico IT | Analista de Ciberseguridad | IAM Junior
CompTIA Security+ (SY0-701)

🔗 [LinkedIn](https://linkedin.com/in/yensinova/)
