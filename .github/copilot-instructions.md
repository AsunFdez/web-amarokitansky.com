# Instrucciones para GitHub Copilot – Migración estática de A.M.A.R.

## 1. Contexto del proyecto

Estoy migrando la página web de la asociación A.M.A.R. (Agenesia Mülleriana y Rokitansky) desde WordPress alojado en Hostinger a una web estática publicada mediante GitHub Pages.

La web original es:

https://amarokitansky.com/

Los archivos actuales proceden de una exportación realizada con el plugin Simply Static de WordPress.

El objetivo es mantener la web original, pero convertirla en una versión estática completamente funcional, sin necesidad de PHP, WordPress ni bases de datos en el servidor.

## 2. Objetivo principal

Revisa todos los archivos de la exportación y corrige los problemas que impidan que la web funcione correctamente en GitHub Pages.

La web debe conservar:

- El diseño y apariencia originales.
- La estructura de navegación.
- Todas las páginas y artículos.
- Las imágenes y fotografías.
- Los estilos CSS.
- Los scripts JavaScript.
- Los enlaces internos y externos.
- Las categorías y etiquetas de los artículos.
- Los enlaces permanentes siempre que sea posible.
- Los metadatos SEO y las etiquetas sociales.
- Las tipografías, iconos y demás recursos gráficos.

No quiero rediseñar la web ni sustituir su contenido.

## 3. Revisión de la estructura

Primero, inspecciona la estructura completa de carpetas y archivos.

Identifica:

- El archivo index.html principal.
- Las páginas HTML individuales.
- La carpeta wp-content.
- Las imágenes dentro de wp-content/uploads.
- Las hojas de estilos CSS.
- Los archivos JavaScript.
- Los recursos del tema Chic Lite.
- Los recursos de plugins.
- Los archivos de fuentes e iconos.
- Los archivos XML, sitemap y robots.txt, si existen.

Comprueba que todas las páginas tengan sus correspondientes archivos y que no existan referencias a recursos inexistentes.

No elimines archivos simplemente porque parezcan innecesarios.

## 4. Reparación de enlaces internos

Uno de los problemas detectados en la exportación es que algunos enlaces entre páginas no funcionan correctamente.

Revisa todos los enlaces HTML de la web.

Comprueba especialmente:

- Menús de navegación.
- Enlaces a páginas interiores.
- Enlaces a artículos.
- Enlaces a categorías.
- Enlaces de paginación.
- Enlaces de navegación anterior y siguiente.
- Enlaces a imágenes y documentos.
- Enlaces del pie de página.

La web utilizará como dominio definitivo:

https://amarokitansky.com/

Adapta las rutas para que funcionen correctamente desde la raíz del dominio.

Ejemplos:

- /sobre-nosotras/
- /blog/
- /wp-content/uploads/2025/05/imagen.jpg

Si las páginas están almacenadas como directorios con index.html, respeta esa estructura.

No conviertas indiscriminadamente todas las URL en archivos .html. Conserva los enlaces permanentes originales cuando sea posible.

Evita que los enlaces internos apunten a:
- Direcciones temporales de GitHub.
- Direcciones de prueba.
- URLs antiguas de WordPress que no deban utilizarse.
- Rutas locales del ordenador.

## 5. Reparación de imágenes

Las imágenes se han descargado correctamente mediante Simply Static y están presentes en la exportación.

Revisa todas las referencias a imágenes en HTML, CSS y JavaScript.

Comprueba:

- Atributos src.
- Atributos srcset.
- Atributos data-src.
- Imágenes de carga diferida (lazy loading).
- Imágenes de fondo CSS (background-image).
- Miniaturas.
- Galerías.
- Imágenes destacadas de los artículos.
- Logotipos e iconos.

Comprueba que cada ruta apunte a un archivo existente.

Presta especial atención a los archivos .webp, .jpg, .jpeg, .png y .gif.

No sustituyas imágenes por otras ni modifiques sus nombres.

Si una imagen no se encuentra, informa de ello y muestra la ruta que está intentando utilizar.

## 6. Compatibilidad con GitHub Pages

La web se publicará en GitHub Pages utilizando un repositorio público y la rama main.

La publicación se realizará desde la raíz del repositorio:

main / (root)

El dominio definitivo será:

amarokitansky.com

Por tanto:

- No debe depender de PHP.
- No debe realizar consultas a bases de datos.
- No debe necesitar WordPress en el servidor.
- No debe depender de rutas locales.
- No debe utilizar rutas relativas que se rompan al navegar entre directorios.
- Debe funcionar con HTTPS.

Comprueba también si existe algún archivo .htaccess o alguna regla de Apache que necesite una alternativa compatible con GitHub Pages.

Añade un archivo .nojekyll en la raíz si no existe.

## 7. Funcionalidades que deben comprobarse

Revisa especialmente:

- Menú principal.
- Menús desplegables.
- Navegación móvil.
- Botones.
- Carruseles.
- Galerías de imágenes.
- Ventanas emergentes.
- Enlaces a redes sociales.
- Formularios de contacto.
- Buscador.
- Paginación del blog.

Si alguna funcionalidad depende de PHP o de la base de datos de WordPress, no intentes simularla de manera insegura.

Identifica la funcionalidad afectada y explica qué alternativa sería necesaria.

El foro de la web está inactivo y no es necesario recuperarlo.

## 8. SEO

Conserva y revisa:

- Títulos de página.
- Meta descriptions.
- Etiquetas canonical.
- Open Graph.
- Twitter Cards.
- Sitemap XML.
- Robots.txt.
- URLs permanentes.

El dominio canónico será https://amarokitansky.com/.

Evita duplicidades entre versiones con www y sin www.

No elimines metadatos SEO existentes.

## 9. Forma de trabajo

Quiero que trabajes por fases.

**Fase 1: Auditoría**

Antes de modificar archivos, inspecciona el proyecto y genera un informe con:

- Estructura de directorios.
- Número de páginas HTML.
- Número de imágenes.
- Enlaces internos detectados.
- Referencias a imágenes inexistentes.
- Errores de rutas.
- Recursos CSS o JavaScript ausentes.
- Funcionalidades incompatibles con GitHub Pages.

**Fase 2: Propuesta de corrección**

Explica qué archivos necesitas modificar y qué cambios propones.

No realices modificaciones masivas sin explicar previamente el alcance.

**Fase 3: Corrección**

Una vez identificados los problemas, corrige las rutas y referencias necesarias.

Mantén el diseño y los contenidos originales.

Evita duplicar archivos o modificar innecesariamente recursos que ya funcionan.

**Fase 4: Verificación**

Comprueba que:

- Todas las páginas HTML tienen sus recursos.
- Las imágenes apuntan a archivos existentes.
- Los enlaces internos son válidos.
- No quedan enlaces a rutas temporales.
- No existen referencias rotas a CSS o JavaScript.
- La navegación funciona desde páginas interiores.
- La web puede publicarse desde la raíz de GitHub Pages.

Genera un informe final con los errores corregidos y los problemas que todavía requieren intervención manual.

## 10. Restricciones importantes

- No reconstruyas la web desde cero.
- No cambies el tema visual.
- No elimines contenidos.
- No cambies las fotografías.
- No renombres imágenes.
- No elimines páginas duplicadas sin comprobar su función.
- No sustituyas funcionalidades por versiones simplificadas sin consultarme.
- No modifiques archivos de WordPress que no sean necesarios para la publicación estática.

La prioridad es conseguir una reproducción fiel de la web original, con todas sus páginas, imágenes y enlaces funcionando en GitHub Pages.

Empieza exclusivamente por la Fase 1: auditoría. Presenta el informe antes de realizar modificaciones.