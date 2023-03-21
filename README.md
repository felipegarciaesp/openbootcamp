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

- **break**: finaliza la ejecución del bucle inmediatamente anterior. En el siguiente ejemplo, el bucle anterior sería el **while** y el **if** sería la condición. Rompe el bucle padre.

```
while contador <= 10:
    print("contador vale", contador)

    if contador == 5:
        break

    contador += 1
```

- **continue**: fuerza la siguiente iteración. Esto signifca que todo lo que hay por debajo del **continue** no se ejecutará y volverá al principio. En el siguiente ejemplo, el **continue** va a provocar que haya un loop infinito atrapado en imprimir "2 es un numero par".
```
contador = 1

while contador <= 10:
    if contador % 2 == 0:
        print(contador, "es un numero par")
        continue
        
    print("Y ahora incremento el contador")
    contador += 1
    
print("Fuera del while")
```

- Ocupar bien el **continue** es una muestra de buena programación. Bien usado es una buena práctica. Lo mismo que **break**, no debemos romper los bucles sin darnos cuenta.

- **for**: es, quizás, la estructura de control más conocida.

- El siguiente es un muy buen ejemplo para utilizar el **for** con **break**:

```
lista = ["hola", "mensaje", "adios"]

for palabra in lista:
    print("Palabra actual:", palabra)

    if palabra == "mensaje":
        print("He encontrado la palabra mensaje")
        break
```

- **switch**: es una conveniencia para comparar una variable con determinados valores y actuar en consecuancia. Hasta Python 3.9 no se podían hacer **switch** en Python. Lo siguiente es la forma de hacer **switch** hasta antes de la versión 3.9 de Python (incluida):

```
valor = 5

if valor == 1:
    print("Valor es 1")
elif valor == 2:
    print("Valor es 2")
elif valor == 3:
    print("Valor es 3")
elif valor == 4:
    print("Valor es 4")
elif valor == 5:
    print("Valor es 5")

```

- **match**: es la palabra reservada que hay en Python para hacer el switch mostrado.

```
valor = 3

match valor:
    case 1:
        print("Valor es 1")
    case 2:
        print("Valor es 2")
    case 3:
        print("Valor es 3")
    case 4:
        print("Valor es 4")
    case 5:
        print("Valor es 5")

```

- El ciclo **for** tiene un **else**. Mucha gente que lleva años programando en Python no lo utiliza, pero hay programadores avanzados que si lo utilizan. El **else** del **for** se ejecuta siempre y cuando el **for** no se haya roto. Un **for** se rompe con **break**. Muy pocos programadores de Python conocen esto. Ejemplo:

```
lista = ["hola", "mensaje", "adios"]

for palabra in lista:
    if palabra == "mensaje"":
        print("Encuentro la palabra mensaje")
        break
else:
    print("No encuentro nada")


```

- Las variables tienen algo llamado **"ámbito"**. Existe el **ámbito global** y el **ámbito de bucle**. El ámbito de una variable depende de donde las ponga. Las variables que se encuentren dentro de un bucle solo las puedo utilizar dentro de ese bucle.

- **pass**: en el momento que se encuentra, pasa (hace nada). Util para ponerlo cuando quiero dejar un bucle, pero aún no tengo claro que poner ahí. Esto evita que se arroje un error. Se utiliza cuando no tenemos claro la implementación de un bucle, método, etc.

```
lista = ["hola", "mensaje", "adios"]

for palabra in lista:
    pass

```