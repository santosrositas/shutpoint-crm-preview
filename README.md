# Shutpoint CRM · Preview de rediseño

Preview navegable del rediseño **visual** del CRM Shutpoint, usado internamente por
Axsis Tecnología. El objetivo es modernizar la interfaz sin alterar la información,
las columnas ni la estructura de contenido del sistema actual.

## Ver el preview

- Publicado: ver la URL de GitHub Pages en la descripción del repositorio.
- Local: abrir `index.html` con doble clic. No requiere servidor ni instalación.

## Vistas incluidas

| Vista | Contenido |
|---|---|
| Dashboard | Accesos rápidos a cada módulo, KPIs, pipeline y compromisos por cerrar |
| Compromisos / Tareas | Folio, responsable, cliente, tipo, fechas, comentarios y estatus |
| Desempeño | 6 KPIs y dos gráficas de cotizaciones concretadas (por responsable y por tipo) |
| Kanban de clientes | Las 6 columnas del pipeline con monto por tarjeta y total por columna |
| Clientes | 5 filtros y las 12 columnas del listado |
| Mercadotecnia | Wizard de campaña: Datos Generales → Contenido → Destinatarios |

Los módulos **Supervisión**, **Servicio al cliente**, **SP Mail** y **Catálogos**
aparecen en el menú pero no se recrearon: no hubo captura de referencia de su
contenido, así que muestran un estado vacío que lo indica en vez de inventar pantallas.

## Sobre los datos

> **Todos los datos son de muestra.** Nombres tipo `Cliente Demo 01` y `Responsable 2`
> son deliberadamente genéricos para que nadie los confunda con información real.
> No hay datos de clientes reales en este repositorio.

Para sustituirlos, editar los arrays al inicio del `<script>` en `index.html`:
`CLIENTES`, `TAREAS`, `KANBAN`, `KPIS`, `CHART_RESP` y `CHART_TIPO`. El dashboard
calcula sus conteos y totales a partir de esos mismos arrays, así que se actualiza solo.

## Estructura

```
index.html                          Preview completo (HTML + CSS + JS, sin dependencias)
assets/                             Logotipos recortados de Shutpoint y Axsis
shutpoint-preview-artifact.html     Versión autocontenida (logos en data URI, sin recursos externos)
```

## Notas técnicas

- Sin build, sin framework, sin dependencias. Un archivo y una carpeta de imágenes.
- Tipografía Inter vía Google Fonts; la versión autocontenida usa la pila del sistema.
- Responsive: sidebar completo en escritorio, colapsado a iconos bajo 1180 px y
  desplegable bajo 900 px.
- Tema claro fijo (`color-scheme: light`), porque reproduce un producto de interfaz clara.
