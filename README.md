# Auditoría QA con Proton VPN local

Aplicación para Windows 10/11 de 64 bits. Realiza una consulta únicamente al pulsar el botón; no hay consultas periódicas ni reintentos automáticos.

## Descarga

[Descargar el paquete completo para Windows](https://github.com/nikotonic/Nwa/raw/refs/heads/main/AuditoriaQA/AuditoriaQA_Windows.zip)

[Configuración Proton en la release](https://github.com/nikotonic/Nwa/releases/tag/auditoria-qa-proton-local-v1.0.0)

## Uso

1. Extrae el ZIP.
2. Ejecuta `DESCARGAR_CONFIG_VPN.bat` una vez para guardar `QA-Proton.conf` desde la descripción de la release, mientras siga publicada allí.
3. Instala [WireGuard para Windows](https://www.wireguard.com/install/).
4. Importa `QA-Proton.conf` y activa el túnel `QA-Proton`.
5. Abre `AuditoriaQA.exe`, confirma el alcance autorizado y pulsa **Ejecutar consulta por VPN**.

El paquete incluye el ejecutable, instrucciones y código fuente en `AuditoriaQA/fuente/`. El ejecutable incluye Python.

La conexión se fija a la interfaz WireGuard local. Sin el túnel disponible, la consulta se bloquea. La configuración limita el túnel al destino de la auditoría.

Los resultados se guardan en `%LOCALAPPDATA%\AuditoriaQAProton\resultados`.

La apertura y el cierre del ejecutable se probaron bajo Wine. Falta la prueba de integración en Windows con el túnel real.

La configuración privada está en la descripción editable de la release y no en el historial Git. Después de guardarla en tu PC, retírala de esa descripción. El ZIP del repositorio no contiene la clave privada.
