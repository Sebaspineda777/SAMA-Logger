# SAMA Logger

Estación autónoma de monitoreo IoT (nivel de río, lluvia, Meteorologicas y Sirena). Este repositorio contiene el
**hardware (PCB)** y el **firmware** de la estación en un solo lugar, para que cada
unidad desplegada en campo pueda rastrearse a una revisión de placa + versión de
código exactas.

## Estructura

```
hardware/   → Proyecto KiCad (esquemático, PCB, gerbers)
firmware/   → Proyecto PlatformIO (ESP32)
docs/       → Notas, diagramas, hojas de datos, registro de despliegues
```

## Estado actual

| Componente | Versión / Revisión | Notas                          |
|------------|--------------------|--------------------------------|
| Firmware   | v1.0.0             | SAMA logger                    |
| PCB        | Rev 1.2            |                                |

## Convenciones de versionado

- **Firmware:** versionado semántico `MAYOR.MENOR.PARCHE` (ej. `1.3.0`).
  - MAYOR → cambio incompatible
  - MENOR → función nueva compatible
  - PARCHE → corrección de errores
- **Hardware:** versionado semántico `MAYOR.MENOR`(ej. `1.0`).
  La revisión va **impresa en el serigrafiado de la placa**.
- Cada estado que se fabrica o se despliega en campo se marca con un **tag** de Git
  (ej. `fw-v1.3.0`, `hw-Rev1.0`).

## Registro de despliegues

| Serie / ID unidad | PCB     | Firmware | Ubicación      | Fecha       |
|-------------------|-------- |----------|----------------|-------------|
| SA-3081           | Rev 1.2 | v 0.1.0  | Necoclí        | 08/09/26    |

