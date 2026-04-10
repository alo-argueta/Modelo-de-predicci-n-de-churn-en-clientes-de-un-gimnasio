# Modelo de predicción de *churn* en clientes de un gimnasio
## Objetivo
Uno de los problemas más comunes que enfrentan los gimnasios y otros servicios es la pérdida de clientes. Para combatir la cancelación en el gimnasio Model Fitness, el presente proyecto busca desarrollar una estrategia de retención de clientes mediante el análisis de los perfiles de clientes. 
## Metodología
### Análisis exploratorio de datos (EDA)
Visualicé y limpié los datos, verificando que no hubiera datos vacíos. Además, tracé histogramas de barras de las características demográficas y de uso para las los usuarios que cancelaron y para los que se quedaron. Aquí pude observar, por ejemplo, que los clientes con contratos extensos (6 y 12 meses) tienen más probabilidad de quedarse.

<img width="1189" height="490" alt="output" src="https://github.com/user-attachments/assets/d1e0edb2-7caf-4eb6-8269-defad65861ca" />


También, para encontrar los factores que más influyen en la cancelación, creé una matriz de correlación. Observé una correlación negativa en la duración del contrato, edad, antigüedad (*lifetime*) y la frecuencia media de visitas por semana durante el mes en curso. Es decir, a medida que estas características aumentaban, la probabilidad de que el cliente cancelara, disminuía. 

<img width="1011" height="904" alt="matriz" src="https://github.com/user-attachments/assets/7d9e2551-88f5-4e7a-85a8-70726bc599c5" />

### Diseño de modelo de predicción de cancelación. 
Desarrollé un modelo de regresión logística y de bosque aleatorio para predecir la cancelación de usuarios el mes siguiente. Comparé ambos modelos utilizando datos de validación, y resultó que el modelo de regresión logística tuvo 1% más de precisión y 2% más de *recall* que el de bosque aleatorio. 
### Creación de clústeres de usuarios
Creé una matriz de distancias con la función linkage () para trazar un dendrograma y así determinar el número ideal de clústeres. Después, segmenté a los clientes en 5 clústeres mediante un modelo de *clustering* con el fin de identificar los grupos con mayor riesgo de cancelación.

<img width="1221" height="838" alt="dendograma" src="https://github.com/user-attachments/assets/d1423d78-2311-4669-8c09-3560e81824bd" />


## Conclusiones
- Se identificaron cuatro factores clave relacionados con la cancelación de clientes: **duración del contrato, edad, antigüedad (*lifetime*) y asistencia a clases**.
- Los contratos cortos están asociados con una mayor tasa de cancelación, mientras que los contratos de 6 o 12 meses favorecen la retención. 
- Los usuarios más jóvenes (27–29 años) presentan mayor probabilidad de cancelar en comparación con usuarios de mayor edad (30–32 años). 
- Los clientes con más tiempo en el gimnasio tienden a permanecer, mientras que aquellos con menos de un mes son más propensos a cancelar. 
- Una mayor asistencia a clases está vinculada con menor cancelación; asistir al menos 2 o 3 veces incrementa la probabilidad de permanencia.
## Recomendaciones
- Incentivar planes largos con descuentos o beneficios.
- Ofrecer promociones para jóvenes (estudiantes, planes grupales).
- Mejorar *onboarding* y atención al cliente para nuevos usuarios.
- Fomentar asistencia con nuevas clases, retos e incentivos.
