# _Comentario:_ Multi-Armed Recommender System Bandit Ensembles

Este paper estudia un sistema híbrido de recomendación que se diferencia por tener en cuenta el carácter cíclico presente en la gran mayoría de recomendaciones. Así, el texto se ecarga de comparar el modelo propuesto con alternativas que no consideran la iteratividad al recomendar, las cuales son bastante comunes en el campo de la investigación.

La forma en la que está estructurado el estudio puede llegar a resultar confusa si no se tienen suficientes conocimientos previos sobre los términos utilizados, esto no necesariamente es un aspecto estrictamente negativo, pero es un factor determinante para acotar el público objetivo del paper, por lo que es necesario mencionarlo. Términos como _bandit_ o _arm_ son utilizados desde el inicio del texto, pero no son definidos hasta la sección 3. Por otro lado, el concepto _multi-armed_ nunca es debidamente explicado en el documento, solo se dan algunos indicios por el contexto del problema planteado.

Respecto a los gráficos utilizados para explicar los resultados del estudio, estos no son del todo efectivos. Si nos basamos en los postulados de Tamara Munzner (2014) en [Visualization Analysis & Design](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.445.9775) el uso de un mismo color tanto para _Matrix factorization_ como para _Dynamic ensemble_ en los gráficos de las figuras 1 y 3 enlaza erróneamente estas dos componentes. En la figura 1, el uso conjunto del color azul parece tener sentido porque el ensamble dinámico elige constantemente _Matrix factorization_, sin embargo en la figura 3 vemos casos donde _Dynamic ensemble_ toma otros caminos, por lo que los resultados son independientes y así deberían mostrarse en los gráficos para una visualización adecuada.

![Figura 3](https://i.imgur.com/ISlRdj2.png)

Adicionalmente, cuando en la sección 4.5 se asegura que en el gráfico inferior derecho de la figura 3 el ganador de _Dynamic ensemble_ cambia entre las primeras 5 _epoch_, realmente esto no se puede verificar en el gráfico mencionado. El nivel de detalle que tienen los gráficos simplemente no permite reconocer claramente lo que ocurre en las primeras 5 épocas, un gráfico adicional que mostrara solo lo que ocurre en las primera 5 épocas de este caso específico habría sido muy beneficioso para sustentar la aseveración. 

Sobre las aportaciones de esta investigación, es claro que pone en perspectiva la importancia de considerar la iteracion al momento de recomenda, dada la gran diferencia entre los resultados mostrados. Sin embargo, este postulado no era del todo nuevo al momento de publicarse este paper, y se había desarrollado en estudios anteriores no mencionados por los autores. Scott (2015), Raj y Kalyani (2017); y Zeng, Wang, Mokhtari y Li (2016) experimentan con _multi‐armed bandit_ considerando el carácter cíclico de las recomendaciones, lo cual (si bien ocurre en contextos diferentes al presentado en este paper) tiene una innegable cercanía con el trabajo de Cañamares, Redondo y Castells, por lo que su mención habría sido correcta para una completa presentación de los trabajos relacionados.

## Referencias

Munzner, T. (2014). Visualization analysis and design. CRC press, Boca Raton, FL. ISBN: 9781466508910

Scott, S. (2015). Multi‐armed bandit experiments in the online service economy. En _Applied Stochastic Models in Business and Industry_, 31, 37– 45, doi: [10.1002/asmb.2104](https://doi.org/10.1002/asmb.2104)

Raj, V. y Kalyani, S. (2017). Taming non-stationary bandits: A Bayesian approach. arXiv preprint. arXiv: [1707.09727](https://arxiv.org/abs/1707.09727)

Zeng, C., Wang, Q., Mokhtari, S. y Li, T. (2016). Online context-aware recommendation with time varying multi-armed bandit. En _Proceedings of the 22nd ACM SIGKDD international conference on Knowledge discovery and data mining_, pages 2025–2034. ACM. doi: [10.1145/2939672.2939878](https://doi.org/10.1145/2939672.2939878)