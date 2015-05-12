---

layout: ots
title: Estructura de Datos en Python

---

Cuando trabajamos con datos necesitamos formas de almacenarlos en variables,
así podemos manipularlos. Usuaremos dos nuevas estructuras de datos que no
cubrimos en la "Introducción a la Programación". Estas son **listas** y
**dicionarios**.

(este capítulo tiene el mismo contenido que el capítulo "Estructuras de Datos
en Python" de el taller "Websites con Python Flask").

Si ya te sientes cómodo con las listas y diccionarios, entonces puedes saltarte
esto e ir al siguiente capítulo.

## Entendiendo las estructuras de datos

En nuestra primera sesión introdujimos tres de los más comunes tipos de datos
usados en programación: números, cadenas y booleanos. Asignamos estos tipos de
datos a variables, una por una:

    x = 3          # números
    a = "gorilas"  # cadenas
    t = True       # booleanos

¿Pero si necesitas algo más complicado, como una lista de compras? Asignar una
variable por cada elemento en la lista haría las cosas muy complicadas:

    item_1 = "leche"
    item_2 = "queso"
    item_3 = "pan"

### Listas

Afortunadamente no necesitamos hacer esto. En vez de ello, tenemos los tipos de
datos `lists` (listas). Una lista vacía es simplemente `[]`:

    lista_compras = []

Cuando estás en el intérprete de Python puedes ver que hay dentro de la lista
con sólo escribir el nombre de la lista. Por ejemplo:

    >>> lista_compras
    []

El intérprete nos muestra que la lista está vacía.

Ahora podemos agregar elementos a ``lista_compras``. Intenta escribiendo los
siguientes comandos en el intérprete de Python:

    lista_compras.append("leche")
    lista_compras.append("queso")
    lista_compras.append("pan")

¿Qué hay en la lista de compras? ¿Qué sucede cuando agregas números o booleanos
a la lista?

También puedes asignar a la lista algunos elementos en ella en una sola línea,
así:

    lista_compras = [ "leche", "queso", "pan" ]

Para remover un elemento de la lista usamos``remove()``:

    lista_compras.remove("leche")

Las listas puedes ser fácilmente procesadas en un ciclo `for`. Mira en este
ejemplo, el cuál imprime cada elemento de la lista en una nueva fila:

    for item in lista_compras:
        print(item)

¡Eso es todo! Python también hace realmente sencillo el revisar si algo está en
la lista o no:

    if "leche" in lista_compras:
        print("¡Delicioso!")

    if "huevos" not in lista_compras:
        print("Bueno, ¡no tenemos eso!")
        lista_compras.append("huevos")

Las listas son la estructura de datos más común en programación. Hay muchas
otras cosas que puedes hacer con las listas, y todos los lenguajes tienen su
propia interpretación ligeramente diferente. Pero fundamentalmente todas son
muy similares.

En resumen:

    lista_compras = []
    lista_compras.append("galletas")
    lista_compras.remove("galletas")

### Diccionarios

El otro tipo de datos principal es el diccionario. El diccionario te permite
asociar una parte de los datos (una "clave") con otra (un "valor"). La analogía
viene de los diccionarios de la vida real, cuando asociamos una palabra (la
"clave") con su significado. Es un poco más difícil de entender que las listas,
pero Python lo hace muy fácil de lidiar con ello.

Puedes crear un diccionario con ``{}``

    comidas = {}

Y puedes agregar items con el diccionario así:

    comidas["platano"] = "¡Delicioso y sabroso!"
    comidas["tierra"]   = "¡No es delicioso, no es sabroso. NO LO COMAS!"

Las claves en este ejemplo son "platano" y "tierra", y los valores son las
cosas que le asignamos. Puedes usar cualquier tipo de datos que no cambie como
una clave de diccionario. Chécalo usando un número, un tipo booleano, una lista
como llave en un diccionario. ¿Qué dice sobre las cadenas?

Como en las listas, siempre puedes ver que hay dentro de un diccionario:

    >>> comidas
    {'platano': '¡Delicioso y sabroso!', 'tierra': '¡No es delicioso, no es sabroso. NO LO COMAS!'}

Puedes mirar una entrada en la diccionario por su clave:

    >>> comidas["platano"]
    '¡Delicioso y sabroso!'

Si la llave no está en el diccionario, ocurre un `KeyError`:

    >>> comidas["queso"]
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    KeyError: 'queso'

Por esta razón, puedes probar cuando una clave está en el diccionario o no,
usando la palabra clave `in`:

    if "queso" in foods:
        print("¡Que es una de nuestras comidas conocidas!")
        print(comidas["cheese"])

`not in` funciona igual, como con las listas.

Puedes borrar en un diccionario. Nosotros realmente no necesitamos incluir una
entrada para tierra:

    del comidas["tierra"]

Lo que hace realmente útiles a los diccionarios es que puedes darle un
significado a sus elementos con ellos. Una lista es sólo una bolsa de cosas,
pero un diccionario es un mapeo específico de algo con algo. Al combinar las
listas con los diccionarios básicamente puedes describir cualquier escructura
de datos en computación.

Por ejemplo, puedes fácilmente agregar una lista a un diccionario:

    ingredientes = {}
    ingredientes["blt sandwich"] = ["pan", "lechuga", "tomate", "tocino"]

O agregar diccionarios a las listas:

    europa = []
    alemania = {"nombre": "Alemania", "poblacion": 81000000}
    europa.append(alemania)
    luxemburgo = {"nombre": "Luxemburgo", "poblacion": 512000}
    europa.append(luxemburgo)

Fuera del mundo Python los diccionarios son frecuentemente llamados `hash tables`, `hash maps` o sólamente `maps` (mapas).

## Siguiente capítulo

Una vez que te sientas cómodo con las listas y diccionarios es tiempo para el
siguiente capítulo, [Introducción a IPython Notebook](notebook.html)
