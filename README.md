# Evento Evaluativo 4 - Machine Learning
## Equipo 8: Clasificación de cobertura forestal (Covertype)



## Descripción del problema

El dataset Covertype tiene 581.012 parcelas de 30 x 30 metros del bosque nacional Roosevelt, en Colorado, descritas con variables cartográficas: elevación, pendiente, orientación, distancias al agua, a vías y a puntos de incendio, sombra, área silvestre y tipo de suelo. Cada parcela tiene uno de 7 tipos de cobertura forestal.

El trabajo tiene dos partes:
- **Supervisado:** predecir el tipo de cobertura de una parcela a partir de sus variables.
- **No supervisado:** buscar grupos de parcelas con características parecidas sin usar la etiqueta, y revisar si esos grupos se relacionan con los tipos de cobertura.

## Integrantes

- Diego Alejandro Gómez Carmona
- Jorge Elias Builes Chavarria
- Juan Pablo Vasquez Tobon
- Sergio Alvarez Hernandez

## Video

Enlace: https://youtu.be/UmXRxIzgsC8

## Estructura del proyecto

```
├── README.md
├── covertype_equipo8.ipynb   notebook con todo el análisis
```

El notebook está organizado así:
1. Descripción del problema
2. Exploración de los datos (EDA)
3. Preprocesamiento
4. Componente supervisado
5. Componente no supervisado
6. Reducción de dimensionalidad
7. Comparación supervisado vs no supervisado
8. Conclusiones

## Instrucciones de ejecución

1. Abrir covertype_equipo_8.ipynb en Google Colab, Jupyter o VS Code.
2. Ejecutar todas las celdas en orden. La primera celda instala ucimlrepo y los datos se descargan solos.
3. La ejecución completa tarda entre 10 y 15 minutos.

Librerías usadas: pandas, numpy, matplotlib, seaborn, scikit-learn, scipy y ucimlrepo.

## Fuente de datos

Blackard, J. (1998). *Covertype* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C50K5N

Se carga con fetch_ucirepo(id=31).

## Principales resultados

- Las clases están muy desbalanceadas: Pino contorta y Picea/Abeto suman el 85% de los datos y Álamo/Sauce solo el 0,47%.
- La elevación es la variable que más separa los tipos de cobertura.
- El mejor modelo fue Random Forest. Con una muestra de 100.000 filas obtuvo un F1 macro de 0,875, frente a 0,821 de KNN y 0.535 de regresión logística.
- Entrenado con todo el conjunto de entrenamiento, el Random Forest llegó a un F1 macro de 0,94. Las clases que peor se predicen son las minoritarias.
- Los grupos encontrados con K-Means, GMM y clustering jerárquico describen perfiles de terreno, pero se parecen poco a los tipos de cobertura ARI 0,004 y 0,017.


