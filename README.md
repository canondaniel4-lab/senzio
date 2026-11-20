# SENZIO

SENZIO es una aplicación web que muestra en tiempo real el consumo de **luz, agua y gas** de un hogar, calcula cuánto cuesta cada servicio y avisa al instante si detecta una fuga. Es la evolución del proyecto "Stellar OS" (`index.html`) hacia la **versión 3.3** (`Version_3.3.html`).

## Qué hace

- Panel con tarjetas de luz (kW / kWh), agua (L/min / litros) y gas (ppm).
- Costo por servicio, gasto total del hogar y comparativa de costos.
- Alertas críticas: agua por encima de 18 L/min o gas por encima de 300 ppm; el gas por debajo de 250 ppm se considera seguro.
- Modo **Simulado** (sin sensores) para probar fugas de agua, de gas y picos eléctricos.
- Conexión **Bluetooth** con una placa ESP32 (modo Hardware).
- Control de relés: luces, válvula de agua y turbinas.
- Registro y acceso en 2 pasos, cuentas con roles y permisos por sección.
- Modo claro u oscuro, cinco colores de acento y guía de uso integrada.
- Descarga del historial en CSV o JSON (hasta 500 registros).

## Cómo ejecutarlo

1. Descarga o clona este repositorio.
2. Abre `Version_3.3.html` en **Google Chrome** o **Microsoft Edge** (la conexión Bluetooth usa Web Bluetooth y solo funciona en esos navegadores).
3. Crea tu cuenta y elige el modo **Simulado** para probar sin sensores, o **Hardware** para vincular la placa ESP32.

No requiere instalación ni servidor.

## Hardware (modo Hardware)

| Servicio | Sensor |
|---|---|
| Luz | Sensor de corriente SCT-013 |
| Agua | Sensor de flujo YF-S201 |
| Gas | Sensor MQ-4 |
| Control | Placa ESP32 con Bluetooth |

## Organización del trabajo

- Tablero en Jira, proyecto **SEN**: https://canondaniel4.atlassian.net/jira/software/projects/SEN/boards/2
- Planeación del Sprint 1: `docs/jira-sprint-1.md`
- Reglas de commits y ramas: `CONTRIBUTING.md`

## Integrantes

| Integrante | Área |
|---|---|
| Valentina Mejía | GitHub |
| Daniel Cañón Céspedes | Jira |
| Dervinson Gabriel Guevara Roa | Entrevistas |
| Miguel Ángel Muñoz Aguirre | Diseño y demo |
| David | Funcionalidad y ensayo |

Proyecto académico, Universidad Cooperativa de Colombia. Profesor: Daniel Flechas.
