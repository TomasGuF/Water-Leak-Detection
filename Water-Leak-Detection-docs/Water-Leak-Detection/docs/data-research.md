# Datos y telemetría — Investigación pendiente

## Dataset candidato
[Smart Meter Water Consumption Measurements](https://zenodo.org/records/7506076), registro de consumo domiciliario de 17 hogares (Alemania). No corresponde a Esval y no se dispone de fugas domésticas reales etiquetadas para este proyecto.

## Checklist antes del desarrollo
- [ ] Descargar una muestra y registrar versión, archivos y licencia.
- [ ] Identificar esquema, unidades, zona horaria y naturaleza de las lecturas (acumuladas o incrementales).
- [ ] Calcular frecuencia efectiva entre lecturas por hogar.
- [ ] Detectar valores faltantes, duplicados, reinicios de contador y saltos.
- [ ] Calcular cobertura por día para evitar estadísticas engañosas.
- [ ] Definir un formato canónico de lectura y pruebas con casos borde.
- [ ] Diseñar replay ordenado temporalmente con velocidad configurable y marca «Simulación».

## Contrato propuesto (por validar)
```json
{
  "household_id": "demo-001",
  "meter_id": "meter-001",
  "recorded_at": "2026-01-01T08:00:00Z",
  "cumulative_volume_liters": 12345.6,
  "source": "simulation"
}
```

Este registro es ilustrativo y NO proviene del dataset. Se validarán semántica y precisión antes de fijar la API.

## Detección explicable
Iniciar con criterios parametrizables de consumo persistente y desviaciones del histórico. Un patrón sospechoso no equivale a una fuga confirmada. Los experimentos sintéticos solo validan el comportamiento bajo condiciones controladas.
