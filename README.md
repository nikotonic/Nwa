# Auditoría QA con Proton VPN local

Aplicación para Windows 10/11 de 64 bits. Realiza una consulta únicamente al pulsar el botón; no hay consultas periódicas ni reintentos automáticos.

## Descarga

[Descargar el paquete completo para Windows](https://github.com/nikotonic/Nwa/releases/download/auditoria-qa-proton-local-v1.0.0/AuditoriaQA_Proton_Local_Windows.zip)

## Uso

1. Extrae el ZIP.
2. Instala [WireGuard para Windows](https://www.wireguard.com/install/).
3. Importa `QA-Proton.conf` y activa el túnel `QA-Proton`.
4. Abre `AuditoriaQA.exe`, confirma el alcance autorizado y pulsa **Ejecutar consulta por VPN**.

El paquete incluye el ejecutable, la configuración Proton y el código fuente en `AuditoriaQA/fuente/`. El ejecutable incluye Python.

La conexión se fija a la interfaz WireGuard local. Sin el túnel disponible, la consulta se bloquea. La configuración limita el túnel al destino de la auditoría.

Los resultados se guardan en `%LOCALAPPDATA%\AuditoriaQAProton\resultados`.

La apertura y el cierre del ejecutable se probaron bajo Wine. Falta la prueba de integración en Windows con el túnel real.

**El ZIP contiene una configuración privada de VPN.** Para retirar esa configuración de GitHub, elimina el archivo ZIP adjunto a la release después de descargarlo; la clave no está guardada en los archivos de este repositorio.
