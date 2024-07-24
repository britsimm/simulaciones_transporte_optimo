# Simulaciones transporte optimo y adaptación de dominio

Como parte de los requisitos para obtener el título de Magister en Ciencia de Datos y Aprendizaje Automático (Facultad de Ingenería, UdelaR) realizé una tesis en Transporte Óptimo y en particular en su aplicación al problema de Adaptación de Dominio. Este repositorio contiene los scripts realizados para experimentar algunas aplicaciones de dichos temas.

### Adaptación de dominio sobre una regresión lineal siempre (Adaptación de dominio supervisada)
Proponemos un método para resolver la adaptación de dominio utilizando transporte óptimo, K-means y SVD cuando los dominios target se obtiene a partir del targer mediante una rotación. El modelo utilizado es una regresión lineal. Como hipótesis tenemos muchos datos en el dominio source pero pocos en el dominio target y queremos aprovechar la gran cantida de datos en source para mejorar la regresión lineal de target. La medida de mejora es el error cuadrático medio. El script ![regresion_rotada.ipynb](https://github.com/britsimm/simulaciones_transporte_optimo/blob/main/regresion_rotada.ipynb) muestra las variantes 1 y 2 del método mientras que el script ![simulacion_procedimiento_propuesto.ipynb](https://github.com/britsimm/simulaciones_transporte_optimo/blob/main/simulacion_procedimiento_proupuesto.ipynb) muestra una situación mas real.

### Adaptación de dominio sobre datos de dígitos: MNIST vs USPS (Adaptación de dominio no supervisada)
Mostramos que entrear un clasificador Support Vector Machine (SVM) en el conjunto MNIST y evaluarlo en USPS no da buenos resultados, lo cual es esperable por ser tener distribuciones distintas. Luego aplicamos transporte óptimo para transportar los datos de MNIST y volvemos a entrenar un SVM en los datos transportados. Mostramos que el nuevo clasificador tiene mejores resultados al evalular en USPS, mostrando así que la aplicación del transporte óptimo en la adaptación de dominio no supervisada puede ser beneficioso.

### Transferencia de color (Transporte óptimo)
Una aplicación interesante del transporte óptimo es la transferencia de color, en donde se busca "copiar" los colores de los pixeles de una imagen a otra, manteniendo la estructura de la imagen de llegada. El script ![transferencia_de_color.ipynb](https://github.com/britsimm/simulaciones_transporte_optimo/blob/main/transferencia_de_color.ipynb) contiene los pasos necesarios para realizar la trasnferencia de color. 

![Transferencia_color_FING](https://github.com/britsimm/simulaciones_transporte_optimo/blob/main/imagenes/transferencia_color.png)


