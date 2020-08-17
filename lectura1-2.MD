# Comentario: _Netflix Update: Try This at Home_

El texto cuenta en primera persona la experiencia de uno de los participantes del [_Netflix Prize_](netflixprize.com) que obtuvo uno de los primeros lugares en los inicios de la competencia. En específico, Simon Funk nos explica los principales aspectos de su programa y algunas de las iteraciones que realizó para llegar a ellos.


Al tratarse de un post dentro de un blog, es interesante verlo como un fragmento de la historia de internet, dado que la lectura (muchas veces informal) te adentra en lo que significó para muchos desarrolladores esta competencia. Esto es mejor cuando agregamos más contexto leyendo primero los posts previos del blog sobre el Netflix Prize (Funk, 2006a; Funk, 2006b).

Respecto a las características del algoritmo de Simon, considero que la más interesante fue la forma en que penalizaba la magnitud de cada característica. Parte de lo anterior en lenguaje C se ve así:
```
userValue [usuario] + = lrate * (err * movieValue [movie] - K * userValue [usuario]);
movieValue [movie] + = lrate * (err * userValue [user] - K * movieValue [movie]);
```
Es más, este fragmento de la publicación se popularizó bastante y sirvió de inspiración para otros desarrolladores. El modelo matemático que se obtiene de esto ha sido mendionado como una optimizacoón del Descenso de Gradiente Estocástico (SGD por sus siglas en inglés),  tal es el caso tanto de Paterek (2007) como de Bell, Koren y Volinsky (2009) que referencian este aporte de Funk como exitoso en la práctica.

Al no tratarse de un paper, si analizamos el texto con una perspectiva académica, falta rigurosidad en los planteamientos y una estructuración general del texto más clara. Definiciones como las de `K=25` o `K=0.02` solo se justifican en que mostraron un mejor desempeño que otros valores al realizar bajo un procedimiento de ensayo y error, sin una argumentación teórica por detrás. El realizar una investigación que incluya componentes teóricos podría mejorar los resultados al dar mayor seguridad de que los valores utilizados son muy probablemente los mejores posibles.

## Referencias

Funk, S. (2006a). Netflix Challenge. Recuperado de: https://sifter.org/~simon/journal/20061027.2.html.

Funk, S. (2006b). Netflix Update: Don't Try This at Home. Recuperado de: https://sifter.org/~simon/journal/20061102.1.html.

Koren, Y, Bell, R. y Volinsky, C. (2009). Matrix Factorization Techniques for Recommender Systems, in _Computer_, vol. 42, no. 8, pp. 30-37, Agosto 2009, doi: [10.1109/MC.2009.263](doi.org/10.1109/MC.2009.263).

Paterek, A. (2007). Improving regularized singular value decomposition for collaborative filtering. Proceedings of KDD Cup and Workshop. Recuperado de: www.cs.uic.edu/~liub/KDD-cup-2007/proceedings/Regular-Paterek.pdf
