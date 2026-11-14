# Cambios principales

- UI: Mejora de la identificación de la música en reproducción (nota musical) en la sesión y en los resultados de búsqueda.
- UI: Mejora del aspecto visual del controlador.
- UI: Eliminación del código restante de la bola de carga oscilante en la pantalla Fusion.
- DEBUG: Corrección de zonas invisibles que podían interceptar clics en la pantalla de inicio: ahora se puede hacer clic en las banderas y los botones incluso cuando Kiki o -BIOPlayer- están encima.
- FUNCIÓN: Mejora de la recuperación del identificador: se genera automáticamente una clave de licencia faltante si la cuenta seguía usando el valor temporal `000-000-000`.
- TECH: Mejora de la publicación de las notas de actualización en GitHub Pages, sin dependencia de `rsync`.
- TECH: Separación de los instaladores Windows por canal: `BIOPlayer`, `BIOPlayer Beta` y `BIOPlayer Dev` ahora pueden coexistir en el mismo equipo.
- UI: Corrección del campo editor de Windows: permanece como `BIOPlayer` para todos los canales.
