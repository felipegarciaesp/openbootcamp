# openbootcamp
Notas de los cursos de OpenBootCamp

# Python

## 3. Tipos de Objetos en Python

### Mutabilidad e Inmutabilidad: 

- Inmutabilidad significa que no lo puedo cambiar, no se modifica la zona de memoria en la que creo la variable. Hay 3 tipos de datos inmutables en Python: **numeros**, **texto** y **tuplas**.

- Mutabilidad significa que lo puedo cambiar, puedo hacer operaciones en ellos. Ejemplos: **listas**, **diccionarios**, **conjuntos**


- Diferencias entre listas y tuplas:
    - La lista es mutable, la tupla es inmutable.
    - Una tupla una vez definida no se puede alterar, la lista sí se puede alterar.
    - La tupla va en paréntesis redondos "( )", mientras que la lista va en corchetes cuadrados "[ ]".
    - Puedo trabajar las listas con operadores y métodos (como .append(), .remove()).


```
diccionario = {
    "clave": "valor",
    "clave2": "valor2"
}
```

- Para eliminar valores de un diccionario se puede utilizar **pop** y **del**. Con el primero se imprime en pantalla el valor que se está eliminando, mientras que el segundo no muestra lo eliminado. El **pop** puede ser útil si, por ejemplo, quiero guardar en otra variable el valor que he eliminado del diccionario.

- `diccionario.pop('clave1')` elimina la clave1 (junto con su valor)

- **Conjuntos o sets**: son listas pero son una sutil diferencia, los conjuntos no muestran valores duplicados mientras que una lista puede repetir elementos. Los elementos de un conjunto se agrupan en este tipo de corchetes: "{ }".

```
lista = [1,2,3,1,2,3]
conjunto = {1,2,3,1,2,3}

(el print del conjunto será: {1,2,3})
```

- Operaciones interesantes con conjuntos, sea `a = {0,2,4,6,8}` y `b = {1,2,3,4,5}`:

    - `a | b` significa "a union b", va a arrojar el conjunto union: `{0,1,2,3,4,5,6,8}`.
    - `a & b` significa "intersección", va a arrojar el conjunto intersección: `{2,4}`.
    - `a - b` significa "diferencia", va a arrojar: `{0,8,6}`. Básicamente, esta operación va a arrojar el conjunto `a` sin los elementos que están en el conjunto `b`.
    - `a ^ b` significa "diferencia simétrica", arroja: `{0,1,3,5,6,8}`. Básicamente arroja los elementos que **no** tienen en comun ambos conjuntos.

## 4. Estructuras de Control

- **Control de Flujo :** El **control de flujo** de un programa lo que hace es guiar la ejecución del mismo.

- **Sentencias Condicionales :** En Python existen dos: **if** y **while**.

- **Puerta XOR :** También llamado **OR exclusiva** es una puerta lógica digital que implementa el **O exclusivo**, es decir, una salida verdadera resulta si una, y solo una de las entradas a la puerta es verdadera.

- ¿Es posible abortar un bucle?: Sí -> **break** y **continue**. Con estos podemos romper la ejecución de un bucle.

- Lo que ocurre dentro de un bucle es la iteración. 

- **break**: finaliza la ejecución del bucle inmediatamente anterior. En el siguiente ejemplo, el bucle anterior sería el **while** y el **if** sería la condición.

```
while contador <= 10:
    print("contador vale", contador)

    if contador == 5:
        break

    contador += 1
```