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
print("La lista de palabras en mayúscula es: " new_words)

3) Crear un Diccionario con List Comprehension
   
Tienes dos listas, una de claves ["nombre", "edad", "ocupación"] y otra de valores ["Juan", 30, "Ingeniero"]. Crea un diccionario
combinando ambas listas usando una List Comprehension.

Solución: 

* se nombran las dos listas 
names = ["nombre", "edad", "ocupation"]
values = ["Juan", 30, "Ingeniero"]

* aqui fusionamos ambas listas creando el diccionario contenido en una lista
new_dict = [dict(zip(names,values))]

* aqui creamos el diccionario con el contenido de las dos listas
diccionario = {names[i]:values[i] for i in range(len(names))}

print("El nuevo diccionario diccionario es: ", diccionario)


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

* Ahora para imprimir dicha matriz sin mostrar las filas en forma de lista
print("La matriz transpuesta es: ")
for fila  in transpond:
   print(" ".join(map(str,fila)))


5) Dado esta lista de diccionarios, necesitarios extraer información de la lista persona.
   
persona = [{
   "nombre": "Raul",
    "edad": 30,
    "ocupacion": "Ingeniero",
    "ciudad": "Madrid"
   }, {
    "nombre": "Juan",
    "edad": 25,
    "ocupacion": "Abogado",
    "ciudad": "Barcelona"
}, {
    "nombre": "Maria",
    "edad": 35,
    "ocupacion": "Médico",
    "ciudad": "Madrid"
}, {
    "nombre": "Pedro",
    "edad": 40,
    "ocupacion": "Profesor",
    "ciudad": "Barcelona"
}, {
    "nombre": "Laura",
    "edad": 28,
    "ocupacion": "Arquitecta",
    "ciudad": "Madrid"
}, {
    "nombre": "Carlos",
    "edad": 32,
    "ocupacion": "Ingeniero",
    "ciudad": "Barcelona"
}, {
    "nombre": "Ana",
    "edad": 27,
    "ocupacion": "Médico",
    "ciudad": "Madrid"
}]


Obtener una lista de nombres de personas que viven en Madrid y la edad sea mayor a 20 años

* Para esto creamos la lista de nombre personas_madrid y dentro hacemos la consulta que necesitamos
  
personas_madrid = [
    persona["nombre"] for persona in persona
    if persona["ciudad"] == "Madrid" and persona["edad"] > 20
]

SALIDA EJERCICIO: ['Raul', 'Maria', 'Laura', 'Ana']


6) Utilización de list Comprehension  con un ELSE

Dado el siguiente listado de números:
   numeros = [1,2,3,4,5,6,7,8,9,10]

transformados = [x*2 if x%2 ==0 else x for x in numeros] 
print("Los números transformados están junto a los que no",transformados]
