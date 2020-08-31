# _Comentario:_ Performance of Recommender Algorithms on Top-N Recommendation Tasks


Este paper **plantea que la métrica RMSE no necesariamente es adecuada para recomendaciones _Top-N_**, esto dado que los resultados expuestos muestran que en muchos casos una mejora en RMSE no implica una mejora real en la precisión. En base a este hallazgo, se proponen dos algoritmos de recomendación que superan a otros algoritmos al ser evaluados exclusivamente por la calidad del _Top-N_ entregado.

En general, me parece positivo que a lo largo de todo el texto se logren explicaciones simples, sin dejar de aportar al estado del arte. El aporte concreto **se diferencia de otros papers**, dado que no se centra en presentar una nueva abstracción de los datos y con ello proponer un nuevo algoritmo más eficiente; aquí se propone una reinterpretación de la forma de evaluar algoritmos y en base a ello propone algoritmos.

En específico, me parece que **los gráficos de las figuras 2, 3, 4 y 5 tienen mucho que mejorar**, dado que la forma de identificar los diferentes algoritmos es bastante confusa. Las diferentes tonalidades de gris simplemente no permiten identificar adecuadamente cada función y los diferentes grosores y separaciones de línea no termina de ser lo suficientemente claro. En muchos casos, como en _PureSVD50_ y _PureSVD150_ las funciones se parecen mucho.

Una posible solución a esto es planteada por Munzner (2014) en _Visualization Analysis & Design_, donde no recomienda usar gradiantes de color (como en este caso) para más de 4 funciones, pero si es util utilizar colores distintos para hasta 9 funciones. Así, la utilización de colores diferentes es útil en este caso, porque solo debemos medir 8 diferentes algoritmos en cada gráfico.

![Imágen Figura 2](https://i.imgur.com/Tu5yl4P.png)

![Imágen Figura 2](https://i.imgur.com/TAO3wUb.png)

A pesar de lo anterior, los gráficos parecen correctos en cuanto a la representación de las mediciones; siendo el problema a criticar de visualización de la información, no de manipulación incorrecta de los datos.

En conclusión, el estudio presenta un cambio de perspectiva respecto a la forma de evaluar Sistemas Recomendadores que parece ser una mejora en cuanto a precisión. Las principales falencias del documento, son en cuanto a la forma de exposición de los datos.

# Referencias

Munzner, T. (2014). Visualization Analysis & Design. Boca Raton: CRC Press.
