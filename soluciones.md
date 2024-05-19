# Soluciones al simulacro

1. La función calculate_average tiene un posible error de división por cero si la lista numbers está vacía. Se puede solucionar agregando una verificación antes de la división.
2. En los métodos area y circumference, radius debe ser self.radius.
3. Respuestas:

- El código define una función find_maximum que toma una lista de números y retorna el número más grande en esa lista. Si la lista está vacía, retorna None.
- No hay errores en el código, pero es ligeramente ineficiente porque compara el primer elemento consigo mismo en el primer paso del ciclo.
- Mejora propuesta:
```python
def find_maximum(numbers):
  if len(numbers) == 0:
    return None
  max_num = numbers[0]
  for num in numbers[1:]:
    if num > max_num:
      max_num = num
  return max_num
```
Justificación: Al empezar el bucle desde el segundo elemento (índice 1), evitamos una comparación innecesaria.
- La complejidad temporal es O(n), donde n es el número de elementos en la lista, ya que el código recorre toda la lista una vez.
- Si numbers es una lista vacía, el código retorna None. Este comportamiento es adecuado, ya que no hay un número máximo en una lista vacía.

4. Respuestas 

- Herencia:
La herencia se observa en cómo las clases Circle y Square extienden la clase base Shape. Esto se logra mediante la palabra clave super(), que se utiliza para llamar al constructor de la clase base desde la clase derivada. La herencia permite que Circle y Square hereden los atributos y métodos de Shape, proporcionando una estructura común y permitiendo la reutilización del código.

- Polimorfismo:
El polimorfismo se presenta en el método area(). Aunque Shape define el método area() como abstracto, cada clase derivada (Circle y Square) proporciona su propia implementación del método area(). Esto permite que el mismo método area() se comporte de manera diferente según el objeto que lo llame. En tiempo de ejecución, se invoca la versión apropiada del método según el tipo del objeto.

- El código implementa herencia y polimorfismo, pero carece de encapsulamiento adecuado. El encapsulamiento se refiere a la ocultación de datos, permitiendo el acceso a través de métodos específicos en lugar de acceder directamente a los atributos. Para implementar el encapsulamiento, se pueden hacer los atributos radius y side_length privados y proporcionar métodos getter y setter para acceder y modificar estos atributos.

Para implementar el encapsulamiento en el código, necesitamos ocultar los detalles internos de los atributos radius y side_length y proporcionar métodos públicos para acceder y modificar estos atributos. El encapsulamiento se logra haciendo que los atributos sean privados, lo que se indica comúnmente mediante un prefijo de doble guión bajo (__) en Python. Esto evita el acceso directo a los atributos desde fuera de la clase, protegiendo así los datos de modificaciones no controladas.

Una vez que los atributos son privados, se deben proporcionar métodos getter y setter. Los métodos getter permiten obtener el valor de un atributo privado, mientras que los métodos setter permiten modificar el valor del atributo de manera controlada, aplicando cualquier validación necesaria. Por ejemplo, podríamos asegurarnos de que el radio (radius) de un círculo sea siempre mayor que cero antes de asignarlo.

5. Respuestas:
- Los elementos están ordenados de manera ascendente, ya que el algoritmo actual compara y cambia de posición los elementos de tal forma que los valores más pequeños se mueven hacia el inicio del arreglo.

- Para cambiar el orden a descendente, se debe modificar la condición en la línea que compara los elementos del arreglo. El cambio sería:
```python
if array[j] < array[j + 1]:  # Cambiar '>' a '<'
    array[j], array[j + 1] = array[j + 1], array[j]
    is_sorted = False
```
- Para adaptar el algoritmo de Bubble Sort a un arreglo bidimensional, podemos seguir una estrategia en dos pasos. Primero, necesitamos ordenar cada fila del arreglo bidimensional de manera individual. Esto implica aplicar el algoritmo de Bubble Sort a cada fila, asegurándonos de que los elementos dentro de cada fila estén ordenados. Este proceso se repite para cada fila del arreglo bidimensional. El objetivo aquí es tratar cada fila como una lista independiente y ordenar los elementos en orden ascendente o descendente según se requiera.

Una vez que cada fila está ordenada, el siguiente paso es ordenar las filas completas en función de un criterio común. En este caso, podemos ordenar las filas basándonos en el primer elemento de cada fila. Al ordenar por el primer elemento, podemos garantizar un orden general en todo el arreglo bidimensional. Para esto, nuevamente utilizamos el algoritmo de Bubble Sort, pero esta vez comparando y cambiando de posición las filas completas en lugar de los elementos individuales dentro de una fila. Es decir, comparamos el primer elemento de una fila con el primer elemento de la fila siguiente y los intercambiamos si es necesario, asegurando así que las filas estén en el orden correcto.

El proceso de ordenar las filas enteras se realiza hasta que no se necesiten más intercambios, lo que indica que las filas están en el orden deseado. Este método garantiza que el arreglo bidimensional esté ordenado de tal manera que tanto las filas como las columnas sigan un orden lógico, facilitando la organización y la búsqueda de datos dentro de la matriz.

