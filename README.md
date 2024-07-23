# Aprendizaje_supervisado_y_no_supervisado

En este repositorio se aplica métodos de aprendizaje supervisado y no supervisado en R. Se utilizó el conjunto de datos `Iris`:

## Implementación de tres métodos de aprendizaje no supervisado

### Reducción de Dimensionalidad:

*Ventajas:*
 - *Facilita la visualización y comprensión de datos complejos, puede mejorar el rendimiento de algoritmos de aprendizaje supervisado.*
 - *Elimina ruido y reduce el riesgo de sobreajuste.*

*Desventajas:*
 - *Puede perder información importante en el proceso de reducción.*
 - *No es siempre intuitivo interpretar los componentes o variables transformadas.*
   
### MDS
 - *Ventajas:*
    - *No necesita de suposiciones previas sobre los datos.*
 - *Desventajas:*
   - *Se trata de un método computacionalmente costoso.*
   - *La elección de los parámetros puede influir en el resultado final.*

- Grafica de MDS para dos componentes: ![](https://github.com/Liliana223/Aprendizaje_supervisado_y_no_supervisado/blob/main/Imagenes%20Iris/MDS2.png)
- Grafica de MDS para tres componentes: ![](https://github.com/Liliana223/Aprendizaje_supervisado_y_no_supervisado/blob/main/Imagenes%20Iris/MDS3.png)

*CONCLUSION:*
*Para este conjunto de datos trabajar con tres dimensiones nos proporcionaría una mayor certidumbre en los datos, ya que explicaría una mayor cantidad de la varianza en los mismos.*

### PCA
 - *Ventajas:*
   - *El PCA elimina correlaciones entre las variables, mejorando la independencia de los datos.*
 - *Desventajas:*
   - *El PCA se utiliza únicamente sobre conjuntos de datos cuyas variables están linealmente correlacionadas.*
   - *Cuando una variable aumente (o disminuya), la otra debe aumentar (o disminuir) en una proporción que sea constante.*

- Grafica de PCA para dos componentes: ![](https://github.com/Liliana223/Aprendizaje_supervisado_y_no_supervisado/blob/main/Imagenes%20Iris/PCA2.png)
- Grafica de PCA para tres componentes: ![](https://github.com/Liliana223/Aprendizaje_supervisado_y_no_supervisado/blob/main/Imagenes%20Iris/PCA3.png)

*CONCLUSION:*
*Para este conjunto de datos trabajar con tres dimensiones nos proporcionaría una mayor certidumbre en los datos, ya que explicaría una mayor cantidad de la varianza en los mismos.*
  
### ISOMAP

*Isomap:*
- *Ventajas:*
  - *Es eficaz con datos cuyas variables mantienen relaciones no lineales.*
- *Desventajas:*
  - *Encontrar el parámetro k es muy difícil, nos puede llevar a determinar distancias incorrectas.*

- Grafica de ISOMAP para dos componentes: ![](https://github.com/Liliana223/Aprendizaje_supervisado_y_no_supervisado/blob/main/Imagenes%20Iris/ISOMAP2.png)
- Grafica de ISOMAP para tres componentes: ![](https://github.com/Liliana223/Aprendizaje_supervisado_y_no_supervisado/blob/main/Imagenes%20Iris/ISOMAP3.png)

*CONCLUSION:*
*Trabajar con tres dimensiones nos proporcionaría una mayor certidumbre en los datos, ya que explicaría una mayor cantidad de la* 
*varianza en los mismos.*
  
## Implementación de tres métodos de aprendizaje supervisado + cálculo de diferentes métricas de evaluación: matriz de confusión precisión, sensibilidad, especificidad. 

Se usaron las dimensiones obtenidas por PCA

```
Model         Accuracy     Kappa
1 SVM            0.9555556  0.9333333
2 SVM Gaussiano  0.8888889  0.8333333
3 Random Forest  0.9111111  0.8666667
4 Naive Bayes    0.8666667  0.8000000
```
### Conclusiones:
*Se analizaron los modelos SVM, SVM Gaussiano, Random Forest y Naive Bayes. De acuerdo al análisis, se obtuvieron los siguientes resultados:*

- *El modelo SVM tiene la mayor precisión y el mayor valor de kappa, siendo el más efectivo y consistente de todos los modelos.*
- *El modelo Naive Bayes tiene los valores Accuracy y Kappa más bajos de todos los modelos comparados, sin embargo puede considerarse razonablemente bueno dependiendo del contexto.*

Grafica el modelo SMV: ![](https://github.com/Liliana223/Aprendizaje_supervisado_y_no_supervisado/blob/main/Imagenes%20Iris/SVM2.png)
