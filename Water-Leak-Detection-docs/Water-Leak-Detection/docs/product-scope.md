# Product Scope — Proyecto personal

## Visión
Aplicación web de monitoreo hídrico residencial que ayuda a comprender el consumo, identificar cambios y revisar anomalías con información clara.

## Usuarios y JTBD
- Cliente residencial (principal): «Cuando mi consumo cambia inesperadamente, quiero conocer cuándo y cuánto cambió, para decidir si debo revisar mis instalaciones».
- Operador o administrador (hipotético, fuera de alcance inicial): supervisar escenarios de demostración.

## Must Have
1. Dashboard con última lectura, fecha de actualización, consumo por día y mes.
2. Gráfico histórico por períodos.
3. Backend que ingiera, valide y consulte telemetría.
4. PostgreSQL y agregaciones comprobables.
5. Reglas configurables para patrones persistentes de consumo.
6. Alertas explicables y recomendaciones; nunca diagnosticar una fuga.
7. Reproducción de lecturas públicas como simulación.

## Should / Could / Won't
- Should: actualización sin recarga, mediante polling o SignalR.
- Could: autenticar usuarios y permitir marcar alertas como revisadas; modelo ML posterior.
- Won't inicial: integración Esval, WhatsApp real, facturación, compensaciones, portal empresarial multipropiedad.

## Hipótesis pendientes
- La experiencia visual ayuda a interpretar variaciones del consumo.
- Un sistema de alertas aporta utilidad sin saturar con falsos positivos.
- El dataset permite suficientes intervalos para monitoreo y pruebas.

## Métricas a medir
Comprensión de alerta, éxito al localizar un aumento, latencia del evento simulado a UI, integridad del almacenamiento y falsas alarmas en escenarios controlados.

## Estado
Solo documentación, sin prototipo funcional ni validación con usuarios. No inferir necesidades internas de Esval.
