# Gestión del proyecto en Jira – Sprint 1 (SENZIO v3.3)

**Responsable de Jira:** Daniel Cañón (tareas 6, 7, 8 y 9 del reparto)
**Espacio Jira:** SENZIO (clave `SEN`, plantilla Scrum)
**Sprint:** Sprint 1 - SENZIO v3.3, del 2 al 6 de noviembre de 2026
**Objetivo del sprint:** Entregar SENZIO v3.3 con el repositorio en GitHub, el tablero de Jira al día, los hallazgos de las entrevistas enlazados y la demo del viernes 6 de noviembre.

## Organización del tablero

- **Estados:** Por hacer → En curso → Listo
- **Épicas (una por área):**
  - SEN-1 GitHub (Valentina)
  - SEN-2 Jira (Daniel)
  - SEN-3 Entrevistas (Gabriel)
  - SEN-4 Diseño / Interfaz (Miguel)
  - SEN-5 Funcionalidad / Lógica (David)
- Cada tarjeta tiene **criterios de aceptación**, **estimación en puntos de historia** y **responsable**.

## Historias de usuario: mejoras de Stellar OS (index.html) a SENZIO v3.3 (Version_3.3.html)

| Clave | Historia | Responsable | Puntos | Problema detectado en la versión anterior |
|---|---|---|---|---|
| SEN-6 | HU-01: Rediseño de contexto doméstico | Miguel | 5 | Lenguaje espacial ("Datos de órbita", "Oxígeno Vital"); no había tarjeta del hogar ni minigráficas. |
| SEN-7 | HU-02: Modo claro/oscuro, limpieza visual y guía integrada | Miguel | 5 | Orbe flotante con voz y efectos pesados; no había modo claro ni guía de uso. |
| SEN-8 | HU-03: Inicio de sesión y registro en 2 pasos | Miguel | 3 | Solo había una "Clave de Operador", sin registro, y todo ingreso era Administrador. |
| SEN-9 | HU-04: Cuentas, sesiones locales y permisos por rol | David | 5 | No se guardaba nada en el navegador y no había roles. |
| SEN-10 | HU-05: Bluetooth con ESP32 y "¿Qué gasta más?" | David | 8 | Solo datos simulados; no había kWh, litros ni costos. |
| SEN-11 | HU-06: Fugas, simulador y exportación CSV/JSON | David | 5 | No detectaba fugas de agua ni tenía simulador; su botón "CSV" solo mostraba un mensaje y no descargaba nada. |

### Criterios de aceptación

**HU-01:** Como usuario residencial, quiero una interfaz enfocada en el hogar, para entender fácilmente mis consumos de luz, agua y gas.
- Los textos de órbita/oxígeno se reemplazan por Luz (kW), Agua (L/min) y Gas (ppm).
- Hay una tarjeta "Mi Hogar" con nombre y fotografía personalizables.
- Cada sensor muestra minigráficas (sparklines) y su porcentaje de variación.

**HU-02:** Como usuario, quiero alternar entre modo claro y oscuro y contar con una guía que no estorbe, para navegar con fluidez en cualquier dispositivo.
- Se eliminan el orbe flotante con voz y los efectos pesados.
- Hay una barra lateral compacta y un selector de modo claro/oscuro con colores de acento.
- Hay una franja de "Guía de uso" que se puede activar y desactivar, y una campana de notificaciones.

**HU-03:** Como nuevo usuario, quiero un registro dividido en pasos, para crear mi cuenta sin saturarme de campos.
- Paso 1: usuario y contraseña. Paso 2: nombre, correo y rol. Se muestra un indicador de progreso.
- Hay un botón para mostrar u ocultar la contraseña.
- Cada paso valida los datos y muestra mensajes de error.

**HU-04:** Como administrador, quiero permisos por rol y sesiones guardadas localmente, para proteger las vistas críticas.
- Los usuarios y la bitácora de accesos se guardan en localStorage.
- Las vistas se restringen según el rol (Comandante, Ingeniero, Técnico, Seguridad, Operador).
- Desde Configuración se puede editar el perfil y cambiar la contraseña.

**HU-05:** Como propietario del hogar, quiero conectar sensores reales por Bluetooth (o simularlos) y ver el costo de cada servicio, para saber cuál representa mayor gasto.
- La conexión con el ESP32 usa Web Bluetooth y hay un selector Simulado / Hardware.
- Se calculan los acumulados en kWh y litros según el tiempo transcurrido.
- Hay un panel que compara el porcentaje de costo de electricidad, agua y gas.

**HU-06:** Como operador, quiero alertas de fugas, un simulador de emergencias y poder exportar el historial.
- Se activa una alerta crítica si el agua supera 18 L/min o el gas supera 300 ppm.
- Hay un simulador de fugas y picos eléctricos con evaluación por reglas.
- Se guardan hasta 500 registros y se pueden descargar en CSV y JSON.

> **Evidencia:** cada historia (SEN-6 a SEN-11) tiene adjunta en Jira una imagen de antes y después con capturas de Stellar OS y SENZIO v3.3.
>
> **Enlace con las entrevistas:** cada historia se enlazará en Jira con su hallazgo cuando esté lista la tabla de hallazgos (tarea 11, Gabriel).

## Tareas del reparto registradas en Jira

| Clave | Tarea | Responsable | Puntos |
|---|---|---|---|
| SEN-12 | T1 Crear el repositorio y subir el código base | Valentina | 2 |
| SEN-13 | T2 Escribir el README | Valentina | 1 |
| SEN-14 | T3 Agregar al profesor como colaborador | Valentina | 1 |
| SEN-15 | T4 Regla de commits y ramas por funcionalidad | Valentina | 1 |
| SEN-16 | T5 Revisar, aprobar e integrar los pull requests | Valentina | 2 |
| SEN-17 | T6 Crear el proyecto, el backlog y el sprint activo | Daniel | 1 |
| SEN-18 | T7 Crear las historias con criterios, estimación y responsable | Daniel | 3 |
| SEN-19 | T8 Mantener el tablero al día | Daniel | 2 |
| SEN-20 | T9 Dar acceso al profesor en Jira | Daniel | 1 |
| SEN-21 | T10 Tabla de hallazgos de las entrevistas | Gabriel | 3 |
| SEN-22 | T11 Enlazar en Jira cada hallazgo con su historia | Gabriel | 2 |
| SEN-23 | T12 Justificar los hallazgos que se mantuvieron | Gabriel | 1 |
| SEN-24 | T14 Antes y después del diseño | Miguel | 2 |
| SEN-25 | T15 Guion de la demo | Miguel | 2 |
| SEN-26 | T17 Antes y después de la funcionalidad | David | 2 |
| SEN-27 | T18 Ensayo de la demo | David | 1 |

Las tareas 13 (Miguel) y 16 (David) corresponden a las historias HU-01 a HU-03 y HU-04 a HU-06.

**Total del sprint:** 31 puntos en historias de usuario y 27 puntos en tareas.
