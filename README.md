# Guía comercial wowinX · Cómo mantenerla

Guía para Haizea y el equipo comercial. Actualizada el 19 de octubre de 2026, tras trasladarla a su propio repositorio.

**Web publicada:** https://softwowinx.github.io/guia-comercial/  
**Repositorio:** [softwowinx/guia-comercial](https://github.com/softwowinx/guia-comercial) · **Rama:** `main` · **Carpeta:** raíz del repositorio

La dirección antigua (`softwowinx.github.io/hub/guia-comercial/`) redirige a la nueva. Estas instrucciones sirven para trabajar con ChatGPT o con Claude.

## Para empezar mañana con Haizea

1. Abrir la web y mostrar los tres accesos: catálogo, modalidades y documentación.
2. Abrir este README en su propio ChatGPT y pegar el prompt inicial de abajo.
3. Comprobar que su sesión puede leer y escribir en el repositorio.
4. Adjuntar una copia del Excel con unos pocos enlaces y pedir que los incorpore.
5. Abrir la versión publicada y comprobar juntos un producto, un enlace común y una excepción específica.

La primera prueba debe ser pequeña y concreta. No hace falta volver a construir la página.

## Qué necesita Haizea en su ChatGPT

- Acceso autorizado a este repositorio de GitHub.
- Un entorno con herramientas para editar archivos y publicar cambios en GitHub; puede utilizar ChatGPT Work si esas herramientas están disponibles en su cuenta.
- El Excel que quiera incorporar o una descripción concreta del cambio.

**La conexión debe comprobarse en su propia sesión.** Los accesos, archivos adjuntos y contexto de la conversación de Juana no se transfieren a otro chat. Poder leer el repositorio no implica disponer de herramientas para escribir en él.

Si su ChatGPT solo puede consultar GitHub, podrá preparar los archivos modificados, pero la publicación deberá hacerla una persona o un entorno con escritura. El asistente debe indicarlo expresamente y no presentar un archivo descargable como si ya estuviera publicado.

Referencias de OpenAI: [Empezar con ChatGPT Work](https://learn.chatgpt.com/docs/get-started-with-work) y [Trabajar con archivos](https://learn.chatgpt.com/docs/artifacts-viewer). La disponibilidad y los permisos se comprueban en la cuenta utilizada.

## Prompt inicial: copiar en un chat nuevo

```text
Voy a mantener la guía comercial de wowinX.

Repositorio: softwowinx/guia-comercial
Rama de publicación: main
Carpeta: raíz del repositorio
Web: https://softwowinx.github.io/guia-comercial/
Instrucciones: lee primero README.md desde la versión actual de main.

Comprueba si tienes herramientas para leer y escribir en este repositorio.
Si no puedes escribir o publicar, dilo con precisión y prepara lo que sí puedas.

Trabaja sobre la última versión del repositorio, no sobre una copia antigua
ni sobre recuerdos de otro chat. Conserva los cambios que haya hecho el equipo.
Haz únicamente el cambio que te pida, compruébalo y publícalo en main cuando
te lo solicite. Si la rama exige revisión, prepara el cambio mediante una PR
y explica qué falta para que llegue a main.

No cambies el diseño ni otros contenidos salvo que te lo pida.
No modifiques el CRM ni Supabase como consecuencia de editar esta guía.
Al terminar, indica archivos modificados, comprobaciones realizadas y enlace
publicado. Distingue entre código guardado en GitHub y despliegue ya verificado.
```

Después se añade la petición concreta, por ejemplo: «Actualiza esta descripción» o «Incorpora los enlaces del Excel adjunto y publica el cambio».

## Incorporar los enlaces del Excel

Archivo de trabajo: **`wowinx_enlaces_documentacion.xlsx`**.

| Pestaña | Para qué sirve |
| --- | --- |
| Enlaces comunes | URL de un recurso compartido entre varios productos. |
| Por producto | URL específica de un producto; tiene prioridad sobre la común. |

- Rellenar las celdas amarillas y conservar los identificadores.
- Se pueden enviar versiones parciales: no es necesario completar todos los enlaces.
- Una celda vacía no ordena borrar un enlace que ya funciona.
- Si un recurso cambia por modalidad, duplicar la fila, conservar sus identificadores y concretar la modalidad.
- Si dos filas proporcionan destinos incompatibles para la misma combinación, resolver la discrepancia antes de sustituir nada.
- Los «sí/no» del inventario original de Haizea indican si un documento está hecho: **no determinan si aplica al producto**.

El Excel no se importa automáticamente en la web: ChatGPT debe leerlo y modificar los archivos correspondientes. Adjuntar el Excel en un chat tampoco publica cambios por sí solo.

### Prompt para una actualización parcial de enlaces

```text
Adjunto una versión parcial de wowinx_enlaces_documentacion.xlsx.
Lee el README de softwowinx/guia-comercial y trabaja
sobre la última versión de main.

Incorpora las URL cumplimentadas utilizando los identificadores del Excel.
Una URL por producto tiene prioridad sobre la común; si hay una variante
por modalidad, respeta su alcance y no la extiendas a otras modalidades.
Las celdas vacías deben conservar los enlaces actuales.

Muestra los enlaces en las tablas por producto. El Índice de documentos
debe seguir sin enlaces y sin columna de origen.
Distingue los enlaces a plantillas/recursos de los documentos de una
operación concreta; no generalices estos últimos.

Actualiza de forma coherente los otros accesos de la guía cuando el mismo
recurso aparezca allí. No cambies el diseño, las modalidades ni los hitos.
No inventes URL ni conviertas una acción del CRM en un documento.

Comprueba enlaces, filtros, navegación y ausencia de errores de JavaScript.
Si modificas documentacion.js, actualiza su versión en index.html.
Publica en main y verifica el despliegue de GitHub Pages.
Resume qué enlaces has incorporado y cuáles quedan pendientes.
```

## Qué contiene la guía

| Acceso | Contenido |
| --- | --- |
| Qué tenemos para vender | Familias, subfamilias, productos, descripciones y modalidades. |
| Modalidades de venta | Recorridos, hitos, documentos y responsables. |
| Documentación | Necesidades por producto y un índice general de tipos de documentos. |

**Índice de documentos:** únicamente tipo, explicación, etapa, cuándo se necesita y si es compartido o específico. **No debe mostrar enlaces ni origen.**

**Tablas por producto:** aquí sí se muestran los accesos a los recursos correspondientes.

## Archivos que se editan

| Archivo | Función |
| --- | --- |
| `index.html` | Diseño, navegación, catálogo y recorridos por modalidad. Incluye contenido y lógica JavaScript. |
| `assets/documentacion.js` | Tipos de documentos, relaciones por producto, filtros y tablas de documentación. |
| `assets/logo-wowinx.png` | Logo oficial utilizado en la cabecera. |
| `assets/guerrero.png` | Imagen de cabecera y favicon. |
| `README.md` | Estas instrucciones. |

El catálogo está representado tanto en `index.html` como en `assets/documentacion.js`. Cuando se cambie un nombre, una familia, una descripción o una modalidad, revisar ambas representaciones para que sigan siendo coherentes.

El código de enlaces contiene actualmente destinos concretos, como dossiers, Prisma y acciones del CRM. Al incorporar el Excel, mantener identificadores estables y una lógica clara de prioridad entre enlaces comunes, específicos y por modalidad.

## Decisiones que deben conservarse

### Diseño

- Fondo claro y colores lavanda/cian.
- Logo oficial de wowinX a la izquierda e imagen del guerrero a la derecha.
- Cabecera compacta; imagen alineada y con el mismo ancho que la tarjeta de modalidades.
- Tarjetas de catálogo y modalidades con iconos.
- Conservar el favicon y la adaptación a pantallas pequeñas.

### Oferta y modalidades

- Familias madre: BeFootball, Virtual Sports, IMM y wx180.
- Experiencias VR: licencia temporal o fija/anual.
- Temporal con producción es una opción dentro de temporal.
- ASCE: sin contraprestación económica del cliente; sí presupuesto, gestión, producción y logística. Sin venta, facturación ni cobro al cliente.
- wx180 es la productora de vídeo inmersivo 180°. Sus pagos son anticipo y resto a la entrega, sin porcentajes predeterminados.
- OIC tiene dos recorridos: acuerdo con el club y patrocinadores.
- No crear un proceso estándar de coexplotación.
- BePlay son ejercicios extraídos de Academy; ai.dols y otras soluciones pendientes no se deben dar por definidas.

### Procesos y responsables

- Brief de preventa al volver de la reunión.
- Solicitud de build a Prisma después de demostración y antes de propuesta comercial.
- Prisma requiere red de oficina o VPN. Abrir el enlace no acredita enviar el formulario.
- La confirmación manual de envío y el OK de Juana viven en el CRM y bloquean el avance.
- Formación siempre incluida en las licencias y en remoto.
- Producto: builds, pruebas, instalación y activación de licencias.
- Operaciones: formación remota, certificado y soporte.
- Dirección de Producción: espacio físico, montaje, desmontaje y retorno.
- People and Culture: equipos, transporte, viajes y personal.
- Producción y Financiero: cierre de costes. Dirección General: aprobación del presupuesto de producción.
- Legal: contratos. Comercial: cliente, briefs, solicitudes, propuestas, firmas y seguimiento.
- Las acciones sin documento llevan al CRM. No incluir Portal wx180 en las licencias VR.

## Publicación y comprobación

Los cambios que llegan a `main` se publican automáticamente con GitHub Pages (rama `main`, carpeta raíz). La web no necesita una compilación de aplicación.

1. Leer la versión actual de los archivos y revisar el cambio solicitado.
2. Modificar solo lo necesario y comprobar la sintaxis del JavaScript.
3. Revisar visualmente la cabecera y probar los tres accesos.
4. En cambios documentales, probar filtros, índice sin enlaces y enlaces por producto.
5. Guardar un commit descriptivo y publicar en `main`, respetando las protecciones de rama.
6. Comprobar el despliegue y abrir la web publicada. Guardar el commit no basta para afirmar que el cambio ya se ve.

Si se modifica `assets/documentacion.js`, cambiar el parámetro `?v=` de su etiqueta `script` en `index.html` por una versión nueva. Se puede añadir una versión a la URL de la página para comprobar el resultado sin reutilizar una copia antigua.

No sobrescribir trabajo de otra persona: si `main` cambió durante la edición, leer la nueva versión e integrar el cambio.

Si algo sale mal, revertir el commit concreto con GitHub o pedir a ChatGPT que lo revierta conservando los cambios posteriores de otras personas.

## Límite entre esta guía y el CRM

Editar esta web **no sincroniza automáticamente los pipelines del CRM**.

El módulo de oportunidades está en otro repositorio: [softwowinx/CRM_OPPS](https://github.com/softwowinx/CRM_OPPS). Sus hitos y bloqueos también dependen de Supabase.

Una modificación de proceso que deba aplicarse en ambos sitios debe solicitarse como tarea separada y verificarse en cada sistema. Para actualizar textos, diseño o enlaces de esta guía no hace falta modificar la base de datos ni solicitar claves del CRM.
