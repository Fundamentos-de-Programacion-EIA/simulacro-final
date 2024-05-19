# Simulacro para el examen final de fundamentos de programación

1. Analiza la siguiente función y encuentra el error. Explica cómo solucionarlo.

```python
def calculate_average(numbers):
  total = 0
  for number in numbers:
    total += number
  average = total / len(numbers)
  return average
``` 

# Uso de la función
result = calculate_average([1, 2, 3, 4, 5])
print("Average:", result)


2. Analiza la siguiente clase y encuentra el error. Explica cómo solucionarlo.

```python
class Circle:
  def __init__(self, radius):
    self.radius = radius

  def area(self):
    return 3.14 * radius ** 2

  def circumference(self):
    return 2 * 3.14 * radius

```

3. El siguiente código en Python tiene como objetivo encontrar el número más grande en una lista de números enteros. Analiza el código y responde las preguntas a continuación.

```python
def find_maximum(numbers):
  if len(numbers) == 0:
    return None
  max_num = numbers[0]
  for num in numbers:
    if num > max_num:
      max_num = num
  return max_num

numbers = [3, 5, 1, 2, 4, 8]
print(find_maximum(numbers))

```
Preguntas:

- ¿Qué hace el código anterior? Describe su funcionamiento.
- Identifica y explica cualquier error o ineficiencia en el código.
- Propón una mejora para el código y justifica tu respuesta.
- ¿Cuál es la complejidad temporal del código actual? Justifica tu respuesta.
- Si numbers es una lista vacía, ¿qué valor retorna el código? ¿Es este comportamiento adecuado? Explica.

4. Analiza el siguiente código y responde las preguntas a continuación:

```python
class Shape:
    def __init__(self, color):
        self.color = color

    def area(self):
        raise NotImplementedError("Subclass must implement abstract method")

class Circle(Shape):
    def __init__(self, color, radius):
        super().__init__(color)
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2

class Square(Shape):
    def __init__(self, color, side_length):
        super().__init__(color)
        self.side_length = side_length

    def area(self):
        return self.side_length ** 2
```

- Qué conceptos de programación orientada a objetos identificas en el código? Explica cada uno.
- Al código anterior le falta uno de los tres conceptos vistos en clase (herencia, polimorfismo, encapsulamiento). Explica cómo se podría implementar el concepto faltante.


5. El siguiente código define una implementación del algoritmo de ordenamiento Bubble Sort en Python. Analiza el código y responde las preguntas a continuación.
```python
def bubble_sort(array):
    n = len(array)
    for i in range(n):
        is_sorted = True
        for j in range(n - 1 - i):
            if array[j] > array[j + 1]:
                array[j], array[j + 1] = array[j + 1], array[j]
                is_sorted = False
        if is_sorted:
            break
    return array
```

- Identifica si los elementos están ordenados de manera ascendente o descendente. Explica qué cambios harías para revertir el orden.
- Explica cómo usarías este algoritmo o qué le modificarías para que también sirva para ordenar arreglos de dos dimensiones.