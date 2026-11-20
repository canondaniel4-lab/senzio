# Reglas de trabajo en el repositorio

## Ramas

- `main` es la rama estable: **nadie sube directo a main**.
- Cada persona trabaja en su propia rama por funcionalidad, con este formato: `tipo/descripcion-corta`
  - `diseno/modo-claro-oscuro`
  - `func/deteccion-fugas`
  - `docs/jira-sprint-1`
  - `fix/csv-historial`

## Mensajes de commit

Formato: `tipo: descripción en presente, clara y corta`

| Tipo | Cuándo se usa |
|---|---|
| `feat` | Nueva funcionalidad |
| `diseno` | Cambios visuales o de interfaz |
| `fix` | Corrección de un error |
| `docs` | Documentación |
| `refactor` | Reorganizar código sin cambiar lo que hace |

Ejemplos:
- `feat: agrega alerta crítica cuando el agua supera 18 L/min`
- `diseno: agrega modo claro y selector de color de acento`
- `docs: agrega planeación del Sprint 1 en Jira con historias HU-01 a HU-06`

Evitar mensajes como "cambios", "arreglo" o "listo".

## Pull requests

1. Abrir el PR desde tu rama hacia `main` con título y descripción de lo que cambia.
2. Enlazar la tarjeta de Jira (por ejemplo `SEN-8`).
3. **Quien abre el PR no lo aprueba**: lo revisa y aprueba otra persona (responsable: Valentina).
4. Tras la aprobación se integra a `main`.

## Jira

Cada quien mueve sus propias tarjetas: Por hacer → En curso → Listo.
