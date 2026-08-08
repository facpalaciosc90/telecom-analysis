# telecom-analysis 
El objetivo del proyecto: 
El objetivo de esté proyecto ha sido identificar patrones de uso, detectar comportamientos atípicos y comprender qué segmentos de clientes muestran necesidades diferenciadas, con el fin de optimizar la oferta comercial y mejorar la experiencia del usuario.
Los datasets utilizados: 
plans.csv: los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).
users_latam.csv: información de clientes: edad, ciudad, fecha de registro, plan contratado.
usage.csv: el detalle de uso real: llamadas (duración) y mensajes (longitud).
Las etapas del análisis realizadas: 
1.-Validar que los archivos se carguen correctamente, conocer las columnas, tipos de datos, y detectarás posibles inconsistencias. Se revisó el número de filas y columnas de cada dataset usando .shape y se uso .info() en cada dataset para obtener un resumen completo de columnas, tipos de datos y valores no nulos.
2.- Identificación de problemas de calidad de datos. Se utilizo .isna() y .sum() para saber cuantos valores nulos hay por columna para cada dataset. Se usó .mean() para calcular la proporción de nulos por columna para cada dataset.
3.- Limpieza básica de datos. Una vez analizados y detectados los datos erróneos de cada uno de los dataset se procedió a la corrección de ellos como convertir las columnas de fecha a tipo fecha Corregir sentinels y fechas imposibles.
4.- Luego se realizó un resumen de las variables clave de la tabla usage por usuario, creando métricas que representen su comportamiento real de uso histórico. También se realizó un Resumen estadístico por usuario durante el 2024. 
5.- Visualización de distribuciones (uso y clientes) y outliers. Mediante histogramas se visualizaron las siguientes columnas: age (edad de los usuarios), cant_mensajes, cant_llamadas y total_minutos_llamada y así poder Entender visualmente cómo se comportan las variables clave tanto de uso como de clientes, observar si existen diferencias según el tipo de plan, y analizar la forma de la distribución.
Luego se hizo una identificación de outliers se uso boxplots para identificar visualmente outliers en las siguientes columnas age, cant_mensajes, cant_llamadas y total_minutos_llamada
6.- Segmentación de Clientes. (Segmentación de clientes por uso) Se clasificó a cada usuario en un grupo de uso (Bajo uso, Uso medio, Alto uso) basándose en la cantidad de llamadas y mensajes registrados. Se creó  una nueva columna llamada grupo_uso en el dataframe user_profile.  (Segmentación de clientes por edad). Se clasificó a cada usuario en un grupo por edad. Se creó una nueva columna llamada grupo_edad en el dataframe user_profile. Se hizo la visualización de la segmentación por clientes, 
7- Insight Ejecutivo para Stakeholders Traducir los hallazgos del análisis en conclusiones accionables para el negocio, enfocadas en segmentación, patrones de uso y oportunidades comerciales.
Cómo ejecutar el notebook (por ejemplo, abrirlo en Google Colab),
Ejecutar un cuaderno en Google Colab es bastante sencillo. Tienes dos formas principales de hacerlo, según si prefieres usar la interfaz visual o atajos de teclado.
Módulos o Celdas Individuales
Para ejecutar una sola celda de código:
•	Con el mouse: Pasa el cursor sobre la celda y haz clic en el botón de Play ▶ que aparece a la izquierda.
•	Atajo principal: Selecciona la celda y presiona Ctrl + Enter (en Windows/Linux) o Cmd + Enter (en Mac). Esto ejecuta el código y mantiene la selección en la misma celda.
•	Avanzar al ejecutar: Presiona Shift + Enter. Ejecuta la celda actual y selecciona la siguiente (o crea una nueva si estás al final).
Una breve guía de reproducción 
Si deseas correr todo el script en secuencia:
1.	Ve al menú superior y selecciona Entorno de ejecución (o Runtime).
2.	Haz clic en Ejecutar todas (Run all).
3.	Atajo rápido: Ctrl + F9 (o Cmd + F9 en Mac).

