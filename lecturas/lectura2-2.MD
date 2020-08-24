# _Comentario:_ BPR: Bayesian Personalized Ranking from Implicit Feedback


Este paper investiga un método optimizado para recomendaciones personalizadas con retroalimentación implícita, al que llama _BPR-Opt_. Se explica también como aplicar este método dentro de modelos de recomendación ya existentes, como lo son _kNN_ y factorización matricial. En general, se presentan diversas reinterpretaciones de conceptos ya conocidos del Filtrado Colabortivo y se abordan tangencialmente algunas ideas novedosas para los Sistemas Recomendadores de la época.

Sobre las múltiples reinterpretaciones expuestas en el documento, es interesante ver cómo aprovecha elementos de la retroalimentación explícita para optimizarlos a retroalimentación implícita. Un ejemplo que destaca es el criterio de optimización presentado en la sección 5.2:

![w(t)=eˆ(−(at−b))/(1+e−(at−b))](https://latex.codecogs.com/svg.latex?\sum_{(u,i,j)\in{D_S}}{\max(0,1-<w_u,h_i-h_j>)+\lambda_w||W||^2_f+\lambda_h||H||^2_f})

El cual está basado en una expresión inicialmente concebida para retroalimentación explícita, pero que aquí han logrado adaptar para tripletas de datos de retroalimentación implícita. A la vez, este nuevo plantemiento tiene la ventaja de ser más genérico, lo cual es crucial para lograr los resultados presentados al final del paper.

Todas estas referencias a modelos ya conocidos, permite comparar _BPR-Opt_ constantemente con ellos. Así, al presentar los resultados se concluye una mejora general al utilizar el método propuesto, pero también se vislumbra que en contextos diferentes los algoritmos tienen desempeños diferentes. Por lo tanto, cambiar el contexto puede hacer variar el algoritmo más óptimo. Este es el caso mostrado en la Figura 6, donde _BPR-kNN_ da mejores resultados para los datos de _Rossmann_, pero _BPR-MF_ da mejores resultados para _Netflix_.

![Figura 6](https://i.ibb.co/yRFqpky/figura6.png)

Con ejemplos como este se resaltan 2 aspectos. Primero, la necesidad de combinar diversas técnicas de filtrado colaborativo para maximizar el rendimiento (Adomavicius y Tuzhilin, 2005). Segundo, la oportunidad de mejorar aun más los Sistemas Recomendadores al mezclar el Filtrado Colaborativo con otros métodos, proporcionando resultados mucho más contextuales en entornos como los teléfonos inteligentes (Ducheneaut et al., 2009).

Por último, la introducción de aleatoriedad dentro del algoritmo, mencionada en la sección 4.2: _BPR Learning Algorithm_, fue algo novedoso al considerar cuales eran los Sistemas Recomendadores más populares en ese entonces. El texto mostró cómo esto optimiza los algoritmos en muchos casos, lo cual podemos reafirmas por la gran candidad de algoritmos aleatorizados que se utilizan en la actualidad.


# Referencias

Adomavicius, G. y Tuzhilin, A. (2005). Toward the next generation of recommender systems: a survey of the state-of-the-art and possible extensions. En _IEEE Transactions on Knowledge And Data Engineering_, vol. 17, no. 6, pp. 734-749. doi: [10.1109/TKDE.2005.99](doi.org/10.1109/TKDE.2005.99)

Ducheneaut, N., Partridge, K., Huang, Q., Price, B., Roberts, M., Chi, E., Bellotti, V. y Begole, B. (2009). Collaborative Filtering Is Not Enough? Experiments with a Mixed-Model Recommender for Leisure Activities. En Houben, G., McCalla, G., Pianesi, F. y Zancanaro, M. (eds) _User Modeling, Adaptation, and Personalization_. UMAP 2009. Lecture Notes in Computer Science, vol 5535. Springer, Berlin, Heidelberg. doi: [10.1007/978-3-642-02247-0_28](doi.org/10.1007/978-3-642-02247-0_28)
