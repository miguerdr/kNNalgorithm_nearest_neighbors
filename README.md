# kNNalgorithm_nearest_neighbors


## Introdución 

La compañía de seguros Sure Tomorrow quiere resolver varias tareas con la ayuda de machine learning y te pide que evalúes esa posibilidad.

- Tarea 1: encontrar clientes que sean similares a un cliente determinado. Esto ayudará a los agentes de la compañía con el marketing.
- Tarea 2: predecir la probabilidad de que un nuevo cliente reciba una prestación del seguro. ¿Puede un modelo de predictivo funcionar mejor que un modelo dummy?
- Tarea 3: predecir el número de prestaciones de seguro que un nuevo cliente pueda recibir utilizando un modelo de regresión lineal.
- Tarea 4: proteger los datos personales de los clientes sin afectar al modelo del ejercicio anterior. Es necesario desarrollar un algoritmo de transformación de datos que dificulte la recuperación de la información personal si los datos caen en manos equivocadas. Esto se denomina enmascaramiento u ofuscación de datos. Pero los datos deben protegerse de tal manera que no se vea afectada la calidad de los modelos de machine learning. No es necesario elegir el mejor modelo, basta con demostrar que el algoritmo funciona correctamente.

## conclusiones

- No encontramos valores ausentes en los datos
- Hay 153 filas duplicadas, no los eliminamos ya que tienen un identificador en la columna, pueden ser clientes diferente con situaciones similares
- Cambiamos los valores de float a int en la columna age
- Hay valores atípicos en las columnas income, age, family_members e income, estos valores atipicos son pocos y no afecta nuestro DataFrame
- Los datos no escalados, arroja distancias mayores que con los datos escalados
- La distancia con la métrica Manhattan son mayores a los resultados con la distancia Euclidiana.
- insurance_benefits con valor igual a cero, es muy superior
- El modelo kNN realiza mejores predicciones que un modelo aleatorio y funciona mejor con los datos no escalados Las métricas de evaluación RMSE y R2 en el modelo lineal, no se ven afectadas por el escalamiento de datos
	- Los datos después de ofuscar, se ven afectados por una mínima diferencia, ya que si redondeamos los valores, estos son similares
	- El método de ofuscación, no afecta los resultados obtenidos por el método de regresión lineal
