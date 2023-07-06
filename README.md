# C# DEVELOPER

## Bienvenido!

Las instrucciones para la prueba que presentaras hoy son las siguientes:

* Leer con atención la descripción del problema que se presenta a continuación.
* Clonar el repositorio para iniciar el desarrollo.
* Al completar la **seccion 1.1** del problema **realizar un commit** al repositorio.
* Al finalizar la prueba y/o realizar la entrega **subir al repositorio** los cambios realizados.

Ten en cuenta los siguientes aspectos a calificar:

* Documentación _detallada_ del código.
* Uso correcto de los conceptos de la _programación orientada a objetos_.
* Código _organizado_ y _legible_ para otros desarrolladores.

Para completar la prueba contarás con un tiempo de **1 hora**, adicionalmente tendras **15 minutos** para explicar tu desarrollo y responder algunas preguntas.

Por favor, **NO** realices consultas en internet y _solo utiliza las páginas necesarias para acceder al repositorio_.

## Descripción del problema

### Seccion 1.1.

Encontrarás en el repositorio un archivo con la clase **Alergias** y algunos comentarios. Esta clase debe contener el _nombre_ de una persona y sus _alérgias_. Cada alergia tiene un valor de puntuación único según la siguiente lista:

- Huevos : 1
- Cacahuetes: 2
- Mariscos : 4
- Fresas : 8
- Tomates : 16
- Chocolate : 32
- Polen : 64
- Gatos : 128

Una enumeración llamada **Alergeno** ya está declarada y no debe ser alterada.

Combinando las puntuaciones de cada alergia sufrida por una persona se obtiene su _puntuación global de alergia_. Por ejemplo, si alguien es alérgico a los _Mariscos_, las _Fresas_ y el _Polen_, su puntuación de alergia sería **4** (_Mariscos_) + **8** (_Fresas_) + **64** (_Polen_) para un total de **76**.

La clase debe tener:

**Constructores**

Uno o más constructores que permiten las siguientes instancias:

- var maria = new Alergias("Maria") → Maria inicialmente no tiene alergias
- var jose = new Alergias("Jose", 66) → Jose es alérgico a los Cacahuetes(2) y al Polen (64)
- var pedro = new Alergias("Pedro", "Fresas Gatos Cacahuetes") → Pedro es alérgico a los Cacahuetes, las Fresas, y los Gatos.

**Propiedades (_de sólo lectura_)**

- _Nombre_ → Nombre de la persona.
- _Puntuacion_ → Devuelve un valor entero igual a la puntuación de la alergia.

### Seccion 1.2.

Para esta sección se deben adicionar los siguientes _métodos_ a la clase:

**Métodos**

_ToString()_ [_override_] → Devuelve una cadena segun las alergias de la persona. Ejemplos:
- "Pepe no tiene alergias"
- “Juan es alérgico a los Cacahuetes"
- "Sofia es alérgica a los Huevos y al Polen".

_EsAlergicoA()_ → Toma un parámetro de tipo _string_ (por ejemplo, "Polen") o un valor de la lista _Alergeno_ y devuelve _true_ o _false_ si la persona es alérgica o no al dicho alérgeno.

_AdicionarAlergia()_ → Toma un _string_ o un valor del tipo _Alergeno_, como en el caso anterior, y actualiza la propiedad _Puntuacion_ sumando el valor numérico del alérgeno dado.

_BorrarAlergia()_ → Toma un _string_ o un valor del tipo _Alergeno_, igualmente como en el primer caso, y actualiza la propiedad _Puntuacion_ restando el valor numérico del alérgeno dado.

## Ten en cuenta

- El método _ToString()_ debe devolver las alergias en orden de su valor de puntuación.

- La cadena de alergias introducida en el constructor estará separada por espacios y cada palabra coincidirá exactamente con el nombre de uno de los valores de la enumeración _Alergeno_.
