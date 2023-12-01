# Exploración de tendencias en la industria de videojuegos
## Introducción
El siguiente proyecto se enfoca en el análisis y la exploración de datos relacionados con la industria de videojuegos utilizando técnicas de ciencia de datos. La industria de los videojuegos es un mercado en constante evolución, con cambios en las preferencias de los jugadores, avances tecnológicos y competencia feroz entre las diferentes plataformas y géneros.

En este proyecto, se ha recopilado y analizado datos de ventas, críticas de usuarios y críticas de juegos, así como información sobre las plataformas, géneros y clasificaciones de contenido (ESRB). Nuestro objetivo es comprender las tendencias que impulsan el éxito de los juegos y cómo factores como la región, las calificaciones y las plataformas influyen en las ventas y la recepción de los juegos.

A través de análisis detallados y pruebas de hipótesis, hemos obtenido una visión profunda de la industria de los videojuegos, lo que puede ayudar a las empresas a tomar decisiones informadas sobre el desarrollo y la comercialización de juegos. Este proyecto brinda información valiosa sobre las preferencias de los jugadores, la influencia de las calificaciones en las ventas y las diferencias regionales en la industria de videojuegos.



## Cambios en los tipos de datos en el DataFrame df_games

Las columnas en las que los tipos de datos han sido cambiados en el DataFrame df_games son:

year_of_release: El tipo de dato original era float. Se cambió a Int64 (entero con posibilidad de valores nulos) utilizando el método astype('Int64'). Esto se hizo para permitir representar años como enteros y para poder manejar adecuadamente los valores nulos en caso de que no haya un año de lanzamiento registrado para un juego.

user_score: El tipo de dato original era object (cadena) debido a la presencia de valores como 'tbd'. Se cambió a float utilizando la función pd.to_numeric con errors='coerce'. Esto se hizo para convertir las calificaciones de usuarios en valores numéricos de punto flotante, tratando los valores no numéricos (como 'tbd') como NaN para permitir operaciones matemáticas y análisis de datos.

name, genre: Los valores faltantes pueden deberse a la falta de información sobre juegos específicos. Se mantendrán sin cambios.

year_of_release: La ausencia de valores podría deberse a la falta de información sobre el año de lanzamiento de ciertos juegos. Estos valores se registrarán como NaN.

critic_score: La falta de datos puede ser el resultado de la ausencia de calificaciones por parte de críticos, especialmente para juegos menos conocidos. Los valores faltantes se dejarán como NaN.

user_score: En el caso de 'tbd', que significa "To Be Determined", indicando que la calificación de usuario aún no se ha determinado, se convertirá a NaN. Los otros valores faltantes también se considerarán como NaN.

rating: La ausencia de valores podría deberse a la falta de información sobre calificaciones por edad o contenido de algunos juegos. Estos valores se mantendrán como están.



## ¿Son significativos los datos de cada período?
Los datos de cada período son significativos. La variación en la cantidad de juegos lanzados a lo largo de los años, que va desde valores tan bajos como 9 juegos en un año hasta 1427 en otro, indica la influencia de eventos y tendencias específicas en la industria de los videojuegos en esos momentos.


## ¿Son significativas las diferencias en las ventas? ¿Qué sucede con las ventas promedio en varias plataformas?
El diagrama de caja de las ventas globales por plataforma muestra diferencias significativas en las ventas entre las plataformas. Las plataformas como PS3 y X360 tienen ventas promedio más altas, mientras que PS2 y PSP tienen ventas promedio más bajas. Además, se observan valores atípicos que representan juegos extremadamente exitosos. Las ventas en PS4 están en crecimiento, mientras que las plataformas más antiguas muestran una disminución en las ventas. En general, este análisis proporciona información valiosa sobre el rendimiento de las diferentes plataformas en la industria de los videojuegos.



## Observaciones
Basándonos en la información proporcionada y en las correlaciones calculadas entre las puntuaciones de críticos y usuarios con las ventas en la plataforma PS4, podemos obtener las siguientes conclusiones:

Correlación entre Critic Score y Ventas (0.41): Existe una correlación positiva moderada entre las puntuaciones de críticos y las ventas en la plataforma PS4. Esto sugiere que, en general, cuando los juegos en esta plataforma reciben puntuaciones más altas por parte de los críticos, tienden a tener mayores ventas totales.

Correlación entre User Score y Ventas (-0.03): La correlación entre las puntuaciones de usuarios y las ventas en la plataforma PS4 es muy cercana a cero, lo que indica que no hay una relación clara entre las puntuaciones de usuarios y las ventas totales. En otras palabras, las puntuaciones de usuarios no parecen influir significativamente en las ventas de juegos de PS4.

Géneros más rentables: Los géneros más rentables son acción, deportes y disparos en primera persona, que generan mayores ventas totales. Estos géneros son populares y atractivos para un amplio público.

Generalización acerca de géneros con ventas altas y bajas: Los géneros con ventas altas suelen ofrecer experiencias de juego ampliamente populares, mientras que los géneros con ventas bajas suelen ser nicho o menos populares, como aventuras, estrategia y simulación.



## Variaciones en las cuotas de mercado de las plataformas principales en las tres regiones (América del Norte, Europa y Japón)
Las preferencias de las plataformas de juegos varían según la región. En América del Norte y Europa, las consolas de Sony y Microsoft, como Xbox y PlayStation, son populares. En Japón, las plataformas de Nintendo, como la Nintendo DS, son las más preferidas. Estas diferencias en las cuotas de mercado reflejan las estrategias de marketing y las preferencias culturales regionales.



## Las preferencias de género en los videojuegos varían según la región:
América del Norte favorece Action, Sports, Shooter y Platform.

Europa prefiere Action, Sports, Shooter, Racing y Misc.

Japón muestra un interés especial por Role-Playing, además de Action, Sports, Platform y Misc. Estas diferencias se explican por las preferencias culturales y de mercado en cada región.



## Las clasificaciones de ESRB tienen un impacto en las ventas de videojuegos en regiones individuales:

En América del Norte, los juegos clasificados como "E" (Everyone) tienen las ventas más altas, seguidos de "M" (Mature) y "T" (Teen).

En Europa, la clasificación "E" (Everyone) también lidera en ventas, seguida de "M" y "T".

En Japón, la clasificación "E" (Everyone) es la más vendida, seguida de "T" y "M".

Las clasificaciones de ESRB tienen un impacto similar en las ventas de videojuegos en América del Norte, Europa y Japón. Los juegos clasificados como "E" (Everyone) son consistentemente los más vendidos en todas las regiones, seguidos de cerca por las clasificaciones "M" (Mature) y "T" (Teen). Esto sugiere una tendencia global en las preferencias de los jugadores en términos de clasificaciones de contenido.



# Conclusión
Se ha realizado un análisis completo de datos relacionados con la industria de videojuegos utilizando un DataFrame llamado df_games. Las acciones incluyeron la conversión de tipos de datos, el cálculo de ventas por región, género y clasificación ESRB, la exploración de relaciones entre calificaciones y ventas, y la realización de pruebas de hipótesis. Por lo que se puede decir que las conclusiones son:

Las preferencias de las plataformas y géneros varían según la región.

Las clasificaciones ESRB influyen en las ventas en todas las regiones.

La calidad percibida por críticos influye en las ventas de juegos.

No hay diferencia significativa en las calificaciones de usuarios entre Xbox One y PC, pero sí entre Acción y Deportes.

En conjunto, estos hallazgos proporcionan información valiosa para la toma de decisiones en la industria de videojuegos, permitiendo entender las tendencias y preferencias del mercado.