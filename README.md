# Material del Taller

Puedes ver el material del taller traducido en vivo en :
http://esparta.github.io/python-data-intro-es/ y el original en http://opentechschool.github.io/python-data-intro/ .

# LEEME para Contribuidores

Este es un how-to amigable para los contribuidores del curso "Introducción al Procesamiento de Datos con Python" en OpenTechSchool. Primero, una rápida actualización del curso:

> ¿Alguna vez te has encontrado haciendo algo metodológica y repetitivamente con una computadora, y preguntado si no habría una mejor forma de hacerlo? ¿Has tenido alguna vez algunos datos, quizás en archivos de texto o un conjunto de números de los cuales te gustaría saber algunas cosas?

> Sólo necesitarás una laptop y entendimiento muy básico de Python. Si ya has hecho el taller "Introducción a la Programación" sería perfecto.

Este curso está previsto como continuación directa de "Introducción a la Programación". Esto significa que sólo cubre lo básico en lectura, escritura y procesamiento de textos con Python. Los programadores en busca de convertirse en "Científicos de Datos" tendrán que esperar para un curso posterior. :)

# Formato de la Clase

En OpenTechSchool tendemos a ser *prácticos* y *a tu propio ritmo*.

Práctico significa que no estamos mucho con la teoría, y requerimos que las personas entiendan algo completamente antes de usarlo. No estamos esperando que ninguno de los estudiantes se convierta en cientfícos de computación. Generalmente la programación de nuestros estudiantes está en el camino de resolver algunos problemas prácticos. Si desean completarlo con LISP o con una hoja de cálculo, es entéramente de su elección.

A tu propio ritmo significa que proveemos acceso completo a las notas del curso al inicio de la sesión. Entonces los estudiantes pueden progresar individualmente. Algunos estudiantes estarán en ello demasiado rápido, a otros les tomará algun tiempo, y la mayoría terminará el trabajo principal con tiempo de sobra. El trabajo principal debería ser completable por todos. Para mantener las cosas interesantes proveemos varios tópicos adicionales que son enteramente opcionales.

La agenda de la clases luce así:

    1200 - Los estudiantes estarán llegando, escriben sus nombres, configuran su laptop.
    1230 - Introducciones, instrucciones para conectarse al WiFi y ubicación de los cursos.
    1235 - Los estudiantes aprenden cosas.
    1545 - Agradecimientos, quizás algunas demostraciones.

Como puedes ver, la agenda tiene una gran pedazo de "aprender cosas". Nos gusta mantener las cosas libres.

# Guía del Autor

Así que haz fork de este repositorio. La guía está escrita como un sitio de [Jekyll](http://jekyllrb.com/), hospedada en páginas de GitHub. Está configurado para que puedes escribir las páginas en Markdown.  Una guía de markup está más adelante.

El curso está dentro de `core/` o `extras/`. Está ligado en `index.md` en el directorio raíz.

* `core/` cubre las metas básicas del curso. Puedes dejar cualquier imagen en  `core/images/`
* `extras/` ahí está todas las cosas interesantes que la gente puede hacer una vez que hayan completado lo básico.

Es más fácil iniciar con el final. Piensa en un algún tópico divertido e interesante para agregar en los extras. Después puedes copiar este archivo para obtener una idea y formatearla.

# Previsualizando el contenido

Cuando haces push a github, el sitio oficial en http://opentechschool.github.io/python-data-intro queda automáticamente actualizado.

Para generar y ver el sitio (con el correcto CSS, etc) con tu propia computadora, puedes instalar Jekyll y despues ejecutarlo así:


    jekyll --serve --auto
    # o
    jekyll serve --watch

Después navega hacia http://localhost:4000/python-data-intro/index.html para ver el contenido del taller generado. Si dejas el servidor ejecutándose, Jekill regenerará automáticamente el sitio cuando éste cambie.

## Editando texto

* Usamos líneas largas (no saltos de línea en párrafos) para mantener los diffs moderadamente limpios.
* El código está indentado con 4 espacios.
* El HTML/CSS está indentado con 2 espacios.

Yo uso Emacs 24, con markdown-mode (Ubuntu emacs-goodies-el) y gfm-mode (GitHub markdown minor-mode). Configura `longlines-show-hard-newlines` si deseas ver dónde están todos los saltos de línea. Esta configuración es bastante útil:

    (add-to-list 'auto-mode-alist '("\\.md\\'" . markdown-mode))
    (setq-default indent-tabs-mode nil)

En Vim, quizás desees esta configuración:

    set tabstop=4
    set shiftwidth=4
    set expandtab

# Guía Markup

# Sección de primer nivel
## Sección de segundo nivel
### Sección de tercer nivel
#### Sección de cuarto nivel

* Elemento de una lista
  * sub-elemento
  * sub-elemento 2
* Segundo elemento

1. Elemento de lista ordenada
2. Elemento 2 de lista ordenada
3. Elemento 3 de lista ordenada
  * Sub-elemento 1
  * Sub-elemento 2
4. Elemento 4 de lista ordenada
  1. Sub-elemento ordenado 1
  2. Sub-elemento ordenado 2
5. Elemento 4 de lista ordenada


*énfasis de texto* para énfasis

**texto en negritas** para negritas

Obtén literales con `backticks`

    O usa una identación de 4 espacios,
    para obtener un bloque de código,
    que luce bello.

> Haz unas cuantas citas. Puedes realizar reflujo de texto tanto como quieras. El salto de línea es impresionante. Y hecho de triunfos.

[enlaces para nerds](http://slashdot.org)

[enlaces para cosas stuff](section8.html)

Esta es una división horizontal:

******

Si quieres resaltar algún código ruby:

    def foo
        puts 'foo'
    end

Un poco de línea de comandos:

    $ holla holla
    get dolla
    $

Para una lista más completa de los lenguajes mira [highlight.js](http://softwaremaniacs.org/media/soft/highlight/test.html)
