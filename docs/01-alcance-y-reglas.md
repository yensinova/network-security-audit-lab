\# Reglas de Enfrentamiento (Rules of Engagement) y Alcance



\## 1. Autorización y entorno



Este ejercicio se realiza exclusivamente en un entorno de laboratorio virtualizado y controlado, con fines educativos y de desarrollo de habilidades de ciberseguridad.



No se realizarán pruebas contra sistemas, cuentas, redes, direcciones IP o servicios que no pertenezcan explícitamente al laboratorio definido en este documento.



\## 2. Alcance (In-Scope)



\- \*\*Red objetivo:\*\* `10.99.99.0/24`

\- \*\*Máquina auditora:\*\* `10.99.99.10` — Kali Linux

\- \*\*Máquina objetivo:\*\* `10.99.99.20` — Metasploitable 2

\- \*\*Virtualización:\*\* VMware Workstation

\- \*\*Segmentación de red:\*\* VMnet2 (Host-only)



\## 3. Fuera de alcance (Out-of-Scope)



\- Equipo anfitrión Windows 11.

\- Red doméstica, empresarial o pública.

\- Internet.

\- Otros adaptadores virtuales, dispositivos o máquinas no incluidos de forma expresa en el alcance.

\- Cuentas, datos personales y servicios de terceros.



\## 4. Actividades autorizadas



\- Descubrimiento de hosts dentro de la red definida.

\- Enumeración de servicios y versiones.

\- Análisis de vulnerabilidades de la máquina Metasploitable 2.

\- Pruebas de explotación exclusivamente contra `10.99.99.20`.

\- Documentación de evidencias, resultados, riesgos y recomendaciones.



\## 5. Reglas operativas



\- Mantener las máquinas virtuales en una red Host-only aislada.

\- No utilizar NAT ni Bridged para la máquina objetivo.

\- No ejecutar ataques fuera del rango `10.99.99.0/24`.

\- No eliminar, alterar o exfiltrar información fuera de los objetivos del laboratorio.

\- Crear snapshots antes de cualquier prueba que modifique el sistema objetivo.

\- Documentar cada actividad relevante y conservar la evidencia necesaria.



\## 6. Criterio de finalización



La práctica finaliza al completar el reconocimiento, la enumeración, las pruebas autorizadas y el informe final, o de inmediato si se detecta que una acción puede afectar a sistemas fuera del alcance.



\## 7. Contacto y responsable



\- \*\*Responsable del laboratorio:\*\* \Yensi Jesús González Nova

\- \*\*Fecha de creación:\*\* 2026-08-13

\- \*\*Estado:\*\* Laboratorio educativo autorizado

