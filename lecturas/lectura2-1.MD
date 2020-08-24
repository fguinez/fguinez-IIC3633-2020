# _Comentario:_ Collaborative Filtering for Implicit Feedback Datasets


Este paper explica las principales características de la retroalimentación implícita, sus diferencias con la retroalimentación explícita y el cómo aprovechar esta información para la creación de sistemas recomendadores.

El listado de características particulares de la retroalimentación implícita presente en el texto es acertado y completo, esto lo vuelve útil para plantear cualquier problema de retroalimentación implícita independiente de su contexto.

Si bien las suposiciones respecto al comportamiento de los usuarios parecen tener sentido (por ejemplo, que viendo varios programas seguidos en un mismo canal decrece el interés de un programa a otro), habría sido positivo justificar esto en estudios sociológicos y/o psicológicos. En general la retroalimentación implícita necesita mucho más entendimiento del comportamiento humano que la retroalimentación explícita, por lo mismo en papers de este tipo se vuelve más util el referenciar a las ciencias sociales. Sin embargo, todas las referencias de este documento son del mundo de los Sistemas Recomendadores.

Morgan, Shanahan y Signorielli (2002) al hablar del comportamiento de las personas frente a la televisión, puntualizan la existencia de diferencias en el uso de esta tecnología según la cultura. Esto implicaría que, en el caso de estudio presentado en este paper, muchos de los supuestos que se podrían hacer para obtener retroalimentación implícita no son universales para todos los usuarios. Lo anterior genera la necesidad de realizar Filtrado Colaborativo implícito diferenciado según el contexto, siendo diferente la interacción con el televisor de un adulto mayor y un adolescente, o de un australiano y un chileno.

Retomando el caso sobre el decrecimiento del interés en un programa, el cual se representa por:

![w(t)=eˆ(−(at−b))/(1+e−(at−b))](https://latex.codecogs.com/svg.latex?w(t)=\frac{e^{-(at-b)}}{1+e^{-(at-b)}})

*Donde ![w](https://latex.codecogs.com/svg.latex?w) es un ponderador de ![r_ui](https://latex.codecogs.com/svg.latex?r_{ui}) y ![t](https://latex.codecogs.com/svg.latex?t) representa al t-ésimo programa visto en un mismo canal.*

Una posible mejora, podría ser el reajustar los valores previos dependiendo del valor de `t`. En específico, considerando los valores ![a=2](https://latex.codecogs.com/svg.latex?a=2) y ![b=6](https://latex.codecogs.com/svg.latex?b=6) encontrados en la experimentación, sin el reajuste propuesto tendríamos los siguientes ponderadores para diferentes valores de ![t](https://latex.codecogs.com/svg.latex?t):
| t |  w   |
|---|:----:|
| 1 | 0.98 |
| 2 | 0.88 |
| 3 | 0.5  |
| 4 | 0.12 |
| 5 | 0.02 |
| 6 | 0.00 |

Sin embargo, considerando el reajuste propuesto, en caso de tener `t = 3` los pesos a usar serían `0.98, 0.88, 0.5`, pero teniendo `t = 6` los pesos podrían reajustarse por algo del tipo `0.98, 0.5, 0.12, 0, 0, 0`. La suposición detrás de lo anterior, es que se hace más probable que un usuario tenga real interés en el tercer programa si solo vio 3 programas seguidos, versus si vio 6 o más programas. En otras palabras, se podría presuponer que en determinados casos mientras más programas seguidos ve un usuario sin cambiar de canal, más probable es que no exista interés real en los programas con `t > 1`.


# Referencias

Morgan, M., Shanahan, J. y Signorielli, N. (2009). Growing up with television: Cultivation processes en _Media effects: Advances in Theory_ (pp. 50-65). Routledge.
