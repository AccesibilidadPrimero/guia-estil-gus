# Revisión técnica de accesibilidad · GUS

Fecha: 10 de octubre de 2026.

Se ha revisado el código HTML, CSS y JavaScript de la guía, con comprobaciones estáticas y ejecución del cambio de idioma en un entorno simulado. Esta revisión no equivale a una certificación WCAG ni a una prueba con VoiceOver.

## Cambios realizados

| Elemento | Cambio |
| --- | --- |
| Navegación | Destinos de foco para el salto al contenido, el menú y el regreso al inicio. Foco visible con contorno y separación. |
| Estructura | Secciones vinculadas a sus encabezados; un único título principal y jerarquía ordenada. |
| Logotipos | Textos alternativos que distinguen composición y color. Las repeticiones decorativas en las tarjetas tipográficas tienen alternativa vacía. |
| Enlaces | Nombres que distinguen el archivo original por composición y color, y los enlaces a cada familia tipográfica. |
| Muestras tipográficas | Los alfabetos completos siguen visibles; se agrupan con una descripción accesible para evitar una lectura repetitiva carácter a carácter. |
| Idiomas | Idioma del documento, textos, nombres accesibles y estado del selector actualizados en catalán, castellano e inglés. |
| Apertura local | Las referencias a los materiales están integradas en JavaScript; el cambio de idioma no depende de una petición fetch al abrir el HTML localmente. |
| Ampliación | Tamaños tipográficos en unidades relativas, bloques sin alturas rígidas que recorten texto y ajustes de columna en pantallas estrechas. |
| Portada | Capa negra degradada sobre la fotografía: oscura detrás del texto y transparente por encima del bloque. Su altura acompaña los saltos de línea y la ampliación del texto. El contraste final debe verificarse en navegador. |
| Controles | Selector de idioma con área mínima de 44 × 44 píxeles CSS y estado seleccionado visible. |
| Preferencias | Se conserva la reducción de movimiento y se añade tratamiento del foco y selección en colores forzados. |
| Sin JavaScript | Contenido inicial completo en catalán; el selector se oculta si no puede funcionar. |

## Comprobaciones completadas

- Sintaxis JavaScript correcta.
- Cambio de idioma ejecutado en un DOM simulado: textos y etiquetas presentes, idioma correcto y un solo botón seleccionado en las tres versiones.
- HTML de las tres versiones: identificadores únicos, un h1, encabezados sin saltos, imágenes con atributo alt, enlaces con nombre, destinos internos existentes y tablas con encabezados de columna.
- Archivos de imagen referenciados presentes en el paquete.
- Cobertura de las fuentes locales: caracteres de las muestras, acentos y punto medio del catalán presentes.
- Contrastes calculados sobre colores sólidos mediante luminancia relativa sRGB.

| Texto | Fondo | Contraste |
| --- | --- | --- |
| #172B46 | #FFF8E8 | 13,50:1 |
| #2457A7 | #FFF8E8 | 6,62:1 |
| #FFFFFF | #2457A7 | 7,01:1 |
| #386447 | #FFF8E8 | 6,44:1 |
| #FFFFFF | #386447 | 6,81:1 |
| #172B46 | #F28C45 | 5,86:1 |
| #172B46 | #F2C44E | 8,69:1 |

Estas parejas superan 4,5:1 para texto normal sobre fondos sólidos. No se ha medido todo el contenido renderizado ni se han evaluado todas las combinaciones posibles.

## Validación pendiente en navegador y lector de pantalla

No se ha podido ejecutar un navegador de pruebas ni VoiceOver en este entorno. Antes de dar por validada la experiencia, comprobar:

1. Safari con VoiceOver: lectura, navegación por encabezados, regiones y enlaces, selector de idioma y anuncios de cambio.
2. Solo teclado: Tab y Mayús+Tab, Enter en los enlaces, Espacio en los botones y foco visible sin obstáculos ni trampas.
3. Zoom al 200 % y 400 %, ancho de 320 píxeles CSS y ampliación solo de texto: ausencia de pérdida de contenido y de desplazamiento horizontal innecesario.
4. Espaciado de texto personalizado: interlineado 1,5, separación entre párrafos 2 veces el tamaño de fuente, letras 0,12 em y palabras 0,16 em.
5. Colores forzados y preferencia de movimiento reducido en un navegador compatible.
6. Acceso a los originales en Drive y disponibilidad de sus permisos desde una sesión externa.

Referencias de comprobación: https://www.w3.org/WAI/WCAG22/Understanding/link-purpose-in-context.html · https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html · https://www.w3.org/WAI/WCAG22/Understanding/reflow.html

## Actualización · 13 de octubre de 2026

La guía definitiva utiliza Fredoka para titulares y Atkinson Hyperlegible Next para textos. Inter se mantiene como tipografía de la propia guía. Se han retirado las tres alternativas y sus archivos de fuente. Se han comprobado las tres traducciones y el contenido HTML resultante; la validación real con navegador y VoiceOver continúa pendiente.
