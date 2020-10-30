# _Comentario:_ Deep learning based recommender system: A survey and new perspectives
### Parte 2 (desde la sección 3.5)

En esta segunda parte, el estudio aborda otros 7 componentes del _state-of-art_ de las recomendaciones basadas en el _Deep Learning_. Para terminar el texto con un una serie de futuras aristas de investigación en la temática y una breve conclusión.

Sobre las diferentes subsecciones entre 3.5 y 3.11: si las comparamos respecto a la primera mitad de la sección 3, la completitud y faciliad con que son explicados los conceptos se mantiene. A pesar de ello, parece disminuir la cantidad de elementos gráficos de apoyo a las explicaciones. En casi todas las subsecciones hasta la 3.5 vemos diagramas que aportan a un mejor entendimiento del _Deep Learning_ (como los vistos en las figuras mostradas más abajo). Pero en la segunda mitad se ve una clara disminución de estos, estando presentes solo en unas pocas secciones. Por dar un ejemplo, en la sección 3.11 un diagrama habría ayudado mucho a entender más fácilmente algunos de los modelos híbridos expuestos.

![Figura 2 - Sección 3.2](https://imgur.com/BZW3Sju.png)
***Figura 2 - Sección 3.2***
![Figura 5 - Sección 3.3](https://imgur.com/k1xWcBt.png)
***Figura 5 - Sección 3.3***

Respecto de los trabajos futuros, veo como especialmente importante la búsqueda de explicabilidad en las recomendaciones con _Deep Learning_. Al mencionar esto, el texto acierta en las motivaciones indicando las necesidades tanto del usuario como del desarrollador, sin embargo no es totalmente claro explicando todas las actuales formas en que está intentando mejorar la explicabilidad.

Por un lado, una arísta importante es el uso y mejoramiento de los _Attentional Models_, lo cual se menciona con suficiente detalle. Pero, por otro lado, está la elaboración de metodologías que busquen el sentido de una recomendación solo por medio de los _inputs_ y _outputs_. Algunos ejemplos de esta última arísta son: la entrega de feedback por parte del usuario y la utilización de clustering/clasificación, esto se ve en más detalle en papers como [Interpretable Convolutional Neural Networks with Dual Local and Global Attention for Review Rating Prediction](https://dl.acm.org/doi/10.1145/3109859.3109890) de Seo, Huang, Yang y Liu (2017), el carácter de _black-box_ de esta metodología no queda tan explícito en el texto.

Otro trabajo futuro a destacar es el de la sección 4.8, referido a mejorar la forma de evaluacion de los modelos, haciendola más unificada y rigurosa. Este trabajo se diferencia de los otros principalmente en dos aspectos:
1. Solo se podrán mejorar las mediciones con el compromiso y aporte de la gran mayoría de la comunidad investigadora
2. No se necesita realizar grandes innovaciones para lograr uma mejor evaluación, basta con observar otras áreas de investigación y lograr establecer estándares adecuados.

Futuros estudios en una línea similar a [Evaluating recommendation systems](https://link.springer.com/chapter/10.1007/978-0-387-85820-3_8) aportarían a una mejora de esta situación, aun cuando se debe tener presente que el objetivo ya no es diversificar las formas de evaluación, si no que (dentro de esa diversidad) comenzar a crear estándares útiles de medición, lo cual además requiere de voluntad de investigadores y revistas.

En conclusión, estamos ante una antología muy completa para adentrarse en esta incipiente área de investigación. La estructura es clara y cada sección detalla lo suficiente para crearle una visión general al lector y generarle interés en saber más.

## Referencias

Seo, S., Huang, J., Yang, H. y Liu., Y. (2017). Interpretable Convolutional Neural Networks with Dual Local and Global Attention for Review Rating Prediction. En _Proceedings of the Eleventh ACM Conference on Recommender Systems (RecSys '17)_. Association for Computing Machinery, New York, NY, USA, 297–305. doi: [10.1145/3109859.3109890](https://doi.org/10.1145/3109859.3109890)

Guy, S. y Gunawardana, A. (2011). Evaluating recommendation systems. En _Recommender systems handbook_, pp. 257-297. Springer US, 2011. doi: [10.1007/978-0-387-85820-3_8](https://link.springer.com/chapter/10.1007/978-0-387-85820-3_8)