# Datalog Station

Estación autónoma de monitoreo IoT (nivel de río, lluvia, clima, humedad de suelo)
que reporta a las autoridades de gestión del riesgo. Este repositorio contiene el
**hardware (PCB)** y el **firmware** de la estación en un solo lugar, para que cada
unidad desplegada en campo pueda rastrearse a una revisión de placa + versión de
código exactas.

## Estructura

```
hardware/   → Proyecto KiCad (esquemático, PCB, gerbers)
firmware/   → Proyecto PlatformIO (ESP32 / ATtiny85)
docs/       → Notas, diagramas, hojas de datos, registro de despliegues
```

## Estado actual

| Componente | Versión / Revisión | Notas                          |
|------------|--------------------|--------------------------------|
| Firmware   | v1.3.0             | SAMA Datalog                   |
| PCB        | Rev A              |                                |

## Convenciones de versionado

- **Firmware:** versionado semántico `MAYOR.MENOR.PARCHE` (ej. `1.3.0`).
  - MAYOR → cambio incompatible
  - MENOR → función nueva compatible
  - PARCHE → corrección de errores
- **Hardware:** revisiones por letra (`Rev A`, `Rev B`, `Rev C`).
  La revisión va **impresa en el serigrafiado de la placa**.
- Cada estado que se fabrica o se despliega en campo se marca con un **tag** de Git
  (ej. `fw-v1.3.0`, `hw-revB`).

## Registro de despliegues

| Serie / ID unidad | PCB    | Firmware | Ubicación      | Fecha       |
|-------------------|--------|----------|----------------|-------------|
| EST-001           | Rev A  | v1.3.0   |                |             |
