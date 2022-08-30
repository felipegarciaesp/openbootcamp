# openbootcamp
Notas de los cursos de OpenBootCamp

# Python

## 3. Tipos de Objetos en Python

### Mutabilidad e Inmutabilidad: 

- Inmutabilidad significa que no lo puedo cambiar, no se modifica la zona de memoria en la que creo la variable. Hay 3 tipos de datos inmutables en Python: **numeros**, **texto** y **tuplas**.

- Mutabilidad significa que lo puedo cambiar, puedo hacer operaciones en ellos. Ejemplos: **listas**, **diccionarios**


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
