# Simulacion_del_examen-Core-

La tarea es limpiar y explorar los datos para una compañía de tecnología emergente que desarrolla aplicaciones móviles. La empresa quiere mejorar la experiencia del usuario y aumentar la retención de usuarios en sus aplicaciones. Han recolectado datos sobre el uso de sus aplicaciones y quieren entender mejor cómo los usuarios interactúan con sus productos.

Contenido del Proyecto

- `user_app_data.csv`: Datos simulados de usuarios.
- `analisis_app.ipynb`: Código del análisis con visualizaciones y explicaciones paso a paso.
- `README.md`: Este documento explicativo del proyecto.

---

1. Limpieza de Datos

- Se cargaron 300 registros con 7 columnas: ID, versión de app, plataforma, duración de sesión, cantidad de sesiones, país, y feedback.
- Se verificó que **no había valores faltantes ni filas duplicadas**.
- Se **normalizaron** las columnas categóricas (`platform`, `country`, `app_version`) a minúsculas y sin espacios para evitar inconsistencias.
- Se revisaron los datos numéricos, y se confirmó que los valores estaban dentro de rangos esperados (por ejemplo, la duración de sesiones entre 1 y 179 minutos).
- Se decidió **mantener `app_version` como tipo `object`**, para evitar errores como convertir "1.10" en "1.1" al pasarlo a tipo numérico.

---

2. Visualizaciones Univariantes

Se realizaron dos gráficos que analizan una variable a la vez:

Gráfico 1: Usuarios por Plataforma

- Se utilizó un gráfico de barras para comparar la cantidad de usuarios que usan Android o iOS.
- Se observó que **ambas plataformas tienen una cantidad similar de usuarios**.

Gráfico 2: Top 3 Países con Más Usuarios

- Otro gráfico de barras muestra los tres países con más usuarios: **España, México y Francia**.
- Estos países concentran la mayor parte del uso.

---

3. Visualizaciones Multivariantes

Se crearon gráficos para analizar relaciones entre múltiples variables:

Gráfico 1: Duración Promedio por País y Plataforma

- Se agruparon los datos por `country` y `platform`, y se graficó la duración media de sesión.
- Alemania, México y USA tienen **más duración promedio en iOS**, mientras que países como España e Italia muestran valores similares entre plataformas.

 Gráfico 2: Feedback por Versión de App y Plataforma

- Se analizó la puntuación media que los usuarios dieron según la versión de la app y plataforma.
- **Todas las versiones tienen feedback similar**, lo que indica que **no hay una versión mejor o peor claramente**.

---

Conclusiones

- Los datos están limpios, sin errores obvios.
- No se ven diferencias grandes entre plataformas o versiones de app.
- Las sesiones duran entre 50 y 150 minutos en la mayoría de los casos.
- Los usuarios suelen calificar la app de forma positiva en general (feedback promedio alto).
- España, México y Francia lideran en cantidad de usuarios.

---

Herramientas Utilizadas

- **Python 3**
- **Pandas** para el manejo de datos
- **Matplotlib** para visualizaciones
- **Google Colab** como entorno de desarrollo
