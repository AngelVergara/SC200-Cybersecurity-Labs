# 🛡️ Lab 1: Implementación de Defensa de Endpoints

**Fecha:** 30 de Enero, 2026
**Tecnologías:** Azure, Defender for Endpoint, PowerShell

## 1. Resumen
En este laboratorio desplegué una máquina virtual en Azure y realicé el onboarding manual a Microsoft Defender for Endpoint para simular y mitigar amenazas.

## 2. Arquitectura
- **VM:** Windows Server 2019 (Standard_D2as_v4)
- **Región:** West US 2
- **Método de Onboarding:** Script Local (debido a latencia de GPO).

## 3. Pruebas de Seguridad
### Detección de Amenazas
Se ejecutaron dos pruebas exitosas:
1. **EICAR Test:** Detectado y eliminado instantáneamente.
2. **Ataque Fileless:** Script de PowerShell ofuscado.
   - *Resultado:* Alerta de severidad media "Suspicious PowerShell command line".

> [Aquí arrastra tu captura del gráfico del incidente]

### Respuesta a Incidentes (Live Response)
Utilicé la terminal remota para investigar sin RDP:
- Comando `processes` para identificar el PID.
- Comando `remediate process` para terminar la amenaza.

> [Aquí arrastra tu captura de la consola negra]

## 4. Conclusión
Se logró aislar el dispositivo infectado cortando su acceso a red, validando la efectividad de las herramientas de respuesta de Defender.
