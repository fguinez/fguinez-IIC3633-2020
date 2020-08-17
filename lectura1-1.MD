# Comentario: Item-based collaborative filtering recommendation algorithms

Este paper plantea dos desafíos para el Filtrado Colaborativo. Por un lado, **mejorar la escalabilidad** de los algoritmos de filtrado colaborativo; y por otro, **mejorar la calidad** de las recomendaciones. La hipótesis de la investigación es que un filtrado colaborativo basado en items (_item-based_) daría mejores resultados que uno basado en usuarios (_user-based_). Los resultados mostraron que el filtrado _item-based_ aporta una mejora consistente por sobre el _user-based_, sin embargo, no fue una mejora significativamente grande.

De todas formas, al ser un estudio del 2001, este fue uno de los primeros acercamientos a algoritmos _item-based_ en un mundo donde predominaban los _user-based_. Sin duda influyó en el mundo del _E-commerce_, como muestran  Linden, Smith y York (2003) en [_Amazon.com recommendations: item-to-item collaborative filtering_](https://ieeexplore.ieee.org/abstract/document/1167344) al detallar el funcionamiento de las recomendaciones de Amazon. También **abrió la puerta a importantes trabajos** posteriores, como la familia de algoritmos _item-based_ Slope One,  presentada en 2005 por Lemire y Maclachlan en su paper [_Slope One Predictors for Online Rating-Based Collaborative Filtering_](https://epubs.siam.org/doi/pdf/10.1137/1.9781611972757.43), los cuales ganaron mucha popularidad.


Además, es interesante contrastarlo con la actualidad. En el 2019, Raghuwanshi y Pateriya en [_Collaborative Filtering: Techniques in Recommendation Systems_](https://link.springer.com/chapter/10.1007/978-981-13-6347-4_2) hicieron un repaso de los tipos de filtrado colaborativo y su popularidad; aquí se puede contrastar que la variedad de clases de filtrado ha aumentado mucho respecto a las existentes en 2001. Los constantes estudios en torno a la temática, nos llevó a un escenario donde no hay una técnica de filtrado predominante, **cada aplicación es un caso particular** donde la solución óptima requiere una combinación diferente de técnicas.

**Respecto a la forma en que se define la variable `x`** en la sección _Experimental Results_, considero que puede producir errores. Al condicionar el tamaño del conjunto de datos de prueba (_test set_) al tamaño del conjunto de datos de entrenamiento (_training set_) no podemos analizar correctamente las implicaciones de aumentar o disminuir el tamaño de uno de los conjuntos. Por ejemplo, en el caso de los resultados mostrados en la _Figura 7_, una explicación para los buenos resultados de `x = 0.8` podría ser el gran tamaño del _training set_, sin embargo no podemos concluir aquello porque el menor tamaño del _test set_ también puede tener algún efecto no esperado en los resultados.

Para un análisis más detallado de esta situación, **sería necesario probar diferentes tamaños de _training set_ para un mismo tamaño de _test set_**. Esto nos permitiría conocer las implicancias individuales de cada variable. Herlocker et al. (2004) describen en detalle diferentes formas de evaluar correctamente Sistemas Recomendadores en [_Evaluating collaborative filtering recommender systems_](https://dl.acm.org/doi/abs/10.1145/963770.963772).

## Referencias

Herlocker, J., Konstan, J., Terveen, L. y Riedl, J. (2004). Evaluating collaborative filtering recommender systems. ACM Trans. Inf. Syst. 22, 1 (Enero 2004), 5–53. doi: [10.1145/963770.963772](doi.org/10.1145/963770.963772)

Lemire, D. y Maclachlan, A. (2007). Slope One Predictors for Online Rating-Based Collaborative Filtering. Proceedings of the 2005 SIAM International Conference on Data Mining, SDM 2005. 5. doi: [10.1137/1.9781611972757.43](doi.org/10.1137/1.9781611972757.43).

Linden, G., Smith B. y York, J. (2003) Amazon.com recommendations: item-to-item collaborative filtering, in _IEEE Internet Computing_, vol. 7, no. 1, pp. 76-80, Enero-Febrero doi: [10.1109/MIC.2003.1167344](doi.org/10.1109/MIC.2003.1167344).

Raghuwanshi S., Pateriya R. (2019) Collaborative Filtering Techniques in Recommendation Systems. In: Shukla R., Agrawal J., Sharma S., Singh Tomer G. (eds) _Data, Engineering and Applications_. Springer, Singapore. doi: [10.1007/978-981-13-6347-4_2](doi.org/10.1007/978-981-13-6347-4_2)
