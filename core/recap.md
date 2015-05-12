---

layout: ots
title: Resumen de lo esencial de Python

---

Este capítulo es sólo un resumen de alguno de los puntos imporantes del curso
"Introducción a la Programación con Python". Siéntete libre de saltartelo si
aún está fresco en tu memoria.

# Ejecutando Python

Después de instalar satisfactoriamente Python en tu sistema, puedes iniciar el
intérprete interactivo de Python escribiendo `python`en la línea de comandos y
presionando `<Enter>`. Esto te mostrará alguna información de contexto acerca
de python similar a esto:

    Python 3.2.3 (default, Oct 19 2012, 19:53:16)
    [GCC 4.7.2] on linux2
    Type "help", "copyright", "credits" or "license" for more information.
    >>>

En Windows puedes abrir Python a través del Menú Inicio.

Para salir del intérprete de Python, presiona `Ctrl-D`.

Para ejecutar un programa almacenado en un archivo de Python puedes ejecutarlo
desde la línea de comandos:

    python program.py

En Windows puedes ejecutar un archivo de Python haciendo doble-click en él.

# Ciclos

¿Qué hace este código?

    for i in 2, 4, 6, 8:
        print(i)

### Solución

Este código imprime los números pares, desde el 2 hasta el 8, uno por línea.

### Reto extra

Python tiene una función integrada llamada `range` que puede generar
automáticamente un rango de números como \[2, 4, 6, 8\]. Por ejemplo,
`range(1,10)` es una secuencia de números desde 1 hasta el 9 (algo común y
algunas veces confusa  situación de programación donde el número "final" no
está incluido en la secuencia).


    for i in range(1,10):
        print(i)

¿Puedes hacer un `range`equivalente a \[2, 4, 6, 8\]? Para tener algunas
pistas, puedes abrir un intérprete de Python y escribir `help(range)`. Los
detalles útiles están cerca del tope. Presiona 'q' para salir del visor de
ayuda cuando hayas terminado.

# Variables

Puedes usar variables para manipular valores en el código. ¿Qué hace este
código?

    total = 0
    for i in 1, 3, 7:
        total = total + i
    print(total)

### Solución

Este código imprime 11 - la suma de los números 1, 3 y 7.

### Reto extra

Si por alguna razón no quieres usar un ciclo `for`, Python tiene una función
incluida llamada `sum` que te deja pasarlo por alto completamente. Puedes
obtener el mismo resultado con esto:

    print(sum([1,3,7]))

¿Puedes hacer una sentencia de que use ambos `sum` y `range` para imprimr la
suma de los números desde el 1 hasta el 10?

# Funciones

Puedes definir tus propias funciones con parámetros para así reusar algo de
código con algunas pequeñas diferencias. ¿Qué imprime éste código?

    def saluda_a(name):
        print("Hola " + name)

    saluda_a("Miranda")
    saluda_a("Fred")

### Solución

    Hola Miranda
    Hola Fred

# Condicionantes

Puedes usar las sentencias `if` para ejecutar algún bloque de código sólo si
la condición es verdadera. ¿Qué imprime éste código?

    angulo = 5
    if angulo > 0:
        print("Girando según las agujas del reloj")
    elif angulo < 0:
        print("Girando en contra las agujas del reloj")
    else:
        print("Sin girar")

### Solución

    Girando según las agujas del reloj


## Capítulo Siguiente

¿Ya estás bien con Python? Puedes ir al siguiente capítulo, [Estructura de Datos en Python](data.html)
