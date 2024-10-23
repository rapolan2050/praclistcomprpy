# praclistcomprpy
Ejercicios práctica list comprenhension Python

1) Doble de los Números

Dada una lista de números [1,2,3,4,5,6], crea una nueva lista que contenga el doble de cada número usando una List Comprehension.

Solución:
group = [1, 2, 3, 4, 5]
double_nums = [(item * 2) for item in group]

2) Filtrar y Transformar en un Solo Paso

Tienes una lista de palabras ["sol", "mar", "montaña", "rio", "estrella"] y quieres obtener una nueva lista con las palabras que
tengan más de 3 letras y estén en mayúsculas.

Solución: 

palabras = ["sol", "mar", "montaña", "rio", "estrella"]
new_words = [palabra.upper() for palabra in palabras if len(palabra) > 3]

3) Crear un Diccionario con List Comprehension
   
Tienes dos listas, una de claves ["nombre", "edad", "ocupación"] y otra de valores ["Juan", 30, "Ingeniero"]. Crea un diccionario
combinando ambas listas usando una List Comprehension.

Solución: 

# se nombran las dos listas 
names = ["nombre", "edad", "ocupation"]
values = ["Juan", 30, "Ingeniero"]

# aqui fusionamos ambas listas creando el diccionario contenido en una lista
new_dict = [dict(zip(names,values))]

# aqui creamos el diccionario con el contenido de las dos listas
diccionario = {names[i]:values[i] for i in range(len(names))}

4) Anidación de List Comprehensions

Dada una lista de listas (una matriz):
       matriz = [
           [1, 2, 3],
           [4, 5, 6],
           [7, 8, 9]
        ]
Calcula la matriz traspuesta utilizando una List Comprehension anidada.
Solución: 

transpond = [[matriz[j][i] for j in range(len(matriz))] for i in range(len(matriz[0]))]




