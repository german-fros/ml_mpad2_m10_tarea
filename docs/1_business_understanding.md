# Comprensión del Proyecto

## Objetivo del Proyecto

Proyecto 1 - predecir la cantidad de puntos que un equipo acumulará al final de la temporada

Proyecto 2 - agrupar correctamente jugadores con estilo de juego similar


## Contexto del Problema
P1 -
    * (fictício) La directiva de un club uruguayo, junto con su cuerpo técnico, desea diseñar una herramienta que le permita evaluar jornada a jornada el desempeño de su equipo y a qué posiciones en la tabla puede aspirar a final de temporada.

P2 -
    * (fictício) La dirección deportiva de un club uruguayo quiere clasificar a todos los jugadores del fútbol uruguayo según sus características, agrupándolos en diferentes perfiles de jugador


## Criterios de éxito
P1 -
    * MAE <= 6 puntos (≈ 2 partidos de diferencia);
    * R² >= 0.6 (explica al menos el 60% de la variación en puntos);

P2 -
    * Silhouette score >= 0.35 (clusters útiles)


## Supuestos y Restricciones
P1 -
    * Dudas sobre si es suficiente la cantidad de datos de partidos disponible (tres temporadas) para elaborar un modelo efectivo;
    * Ver como se comporta con equipos los cuales tenemos menos datos, debido a su ausencia en alguna de las temporadas

P2 -
    * Nos falta la información de la posición de cada jugador, no permitiéndonos elaborar un perfil mucho más específico | De algunos jugadores vamos a tener más temporadas con datos que otros, necesitando que decidamos como abordar esa cuestión
