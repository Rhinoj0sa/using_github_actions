# Gestión de cambios
Por favor antes de enviar el PR asegúrese  de llenar el siguiente formato:

Por favor incluya un resumen de los cambios y la motivación  de los mismos
<!--- Ingrese un resumen de los cambios y la motivación del mismo-->


# ¿Como a sido probado el query?

Por favor describa las pruebas que ha hecho.
<!--- Ingrese la descripción  de las pruebas -->

Por favor incluya evidencia del dataset resultado.
<!--- Ingrese por favor la liga al dataset generado por el query -->

Por favor incluir un listado de las tablas fuente del query.
<!--- Por favor incluya un listado de las tablas fuente e indicar si están  a punto de deprecar -->

En caso de modificar los cálculos  de la query (optimización  o cambio)
<!--- Por favor indique la motivación  del cambio de cálculo  -->


# Checklist:

- [ ] Incluir un resumen de los cambios realizados
- [ ] He probado el query 
- [ ] He dejado evidencia de que el query corre ok (dataset) 
- [ ] He dejado un listado de las tablas fuente
- [ ] He dejado documentada la motivación  del cambio de los calculos





## Descripción del Merge Request
¿Qué cambios introduce este Merge Request?
Genera una validacion sobre el query que genera un universo este contenido en el universo de feature store.

## Puntos importantes a revisar:

## Consideraciones adicionales:
Ver historia: [MLCA-2844]

## Estrategia de Merge y Manejo de Ramas

- **Ramas Hotfix y Features:** Squash and Merge
- **Ramas Release y Backports:** Merge común

## Checklist de Revisión de Código:

### Arquitectura Hexagonal
- [ ] ¿Los casos de uso tienen responsabilidad única?
- [ ] ¿La lógica está contenida únicamente en los casos de uso?
- [ ] ¿Los casos de uso funcionan correctamente cuando se llaman desde otros lugares?
- [ ] ¿La única conexión con el exterior es manejada por adaptadores/API?

### Calidad del Código
- [ ] ¿Cumple con los estándares de calidad de código de Fury?
- [ ] ¿El código es elegante y limpio?
- [ ] ¿Se utilizan linters?
- [ ] ¿Las clases/métodos/funciones tienen nombres claros y descriptivos?
- [ ] ¿El código evita efectos secundarios inesperados?
- [ ] ¿Las funciones son elegantes y bien estructuradas?
- [ ] ¿Las excepciones se manejan adecuadamente?

### Criterios de Finalización
- [ ] ¿El trabajo puede considerarse como DONE?
- [ ] ¿Se alcanzan los criterios de aceptación de la tarea?
- [ ] ¿Hay algo que pueda ser capitalizado como activo?

### Documentación y Deuda Técnica
- [ ] ¿Se actualizó la documentación relevante?
- [ ] Changelog
- [ ] Confluence
- [ ] Gráficos
- [ ] ¿Se adquirió deuda técnica? ¿Fue registrada correctamente?
- [ ] ¿Hay algo interesante en la implementación para registrar en la Retrospectiva Técnica?

### Friendly reminder


[MLCA-2844]: https://mercadolibre.atlassian.net/browse/MLCA-2844?atlOrigin=eyJpIjoiNWRkNTljNzYxNjVmNDY3MDlhMDU5Y2ZhYzA5YTRkZjUiLCJwIjoiZ2l0aHViLWNvbS1KU1cifQ
