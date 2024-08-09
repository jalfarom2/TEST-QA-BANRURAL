Archivo: index.html
Tipo de prueba: Manual

Revisión de código:
Línea 49: no tiene el ‘.’ antes del nombre del class, tendría que ser entonces '.lowOrHi'. Se realiza la corrección.
Línea 87: addeventListener está mal escrito, debería de ser addEventListener. Se realiza la corrección.
Línea 95: addeventListener está mal escrito, debería de ser addEventListener. Se realiza la corrección.

Casos de Prueba:

    Prueba 1: 
    Descripción de la prueba: El numero generado aleatoriamente tiene que ser un numero entero entre 1 al 100.
    Resultado esperado: El número que se genera es de entre el rango del 1 al 100. 
    Estado de la prueba: Insatisfactorio.
    Resultado obtenido: El número que se genera es de tipo float de entre 0 al 10.
    Correcciones: Se agrego la función 'Math.floor' para que elimine los valores decimales del número entregado por la función 'Math.random'.
                  Se cambio el valor '10' por '100' para aumentar el rango de números aleatorios.
                  Se suma '1' al valor entregado por la función, ya que puede entregar como resultado el número 0 y como máximo el 99. Al agregar la suma
                  ya se ajusta al rango de 1 a 100 solicitado.

    Prueba 2:
    Descripción de la prueba: Se ingresa un valor que no sea un numero entero.
    Resultado esperado: La aplicación muestra un mensaje indicando que el usuario ingreso un valor no valido y no es tomado en cuenta como un intento utilizado.
    Estado de la prueba: Insatisfactorio.
    Resultado obtenido: La aplicación acepta el valor ingresado por el usuario y gasta un intento.
    Correcciones: Se creo la función 'checkUserGuess' para que compruebe que el valor ingresado por el usuario sea el solicitado por el programa.
                  Se agrego condicional If para validar si el campo 'userGuess' se encuentra vacío.
                  Se agrego condicional If para validar el valor ingresado en 'userGuess'.

    Prueba 3:
    Descripción de la prueba: Se ingresa un número mayor al número a adivinar.
    Resultado esperado: Se debe mostrar el siguiente mensaje en color negro: "Incorrecto! ¡El número es mayor!".
    Estado de la prueba: Insatisfactorio.
    Resultado obtenido: El mensaje se muestra en color verde.
    Correcciones: Se realizo la corrección del color a negro. 

    Prueba 4:
    Descripción de la prueba: Se ingresa un número menor al número a adivinar.
    Resultado esperado: Se debe mostrar el siguiente mensaje en color negro: "Incorrecto! El número es menor!".
    Estado de la prueba: Insatisfactorio.
    Resultado obtenido: El mensaje se muestra en color verde.
    Correcciones: Se realizo la corrección del color a negro.

    Prueba 5:
    Descripción de la prueba: Se agotan los 10 intentos que tiene el usuario.
    Resultado esperado: Se debe mostrar el mensaje de color rojo: "!!!Pérdistes!!!".
    Estado de la prueba: Insatisfactorio.
    Resultado obtenido: El programa solo deja realizar 5 intentos.
                        ¡Cuando se agotan los intentos, se muestra el mensaje ‘Felicitaciones! adivinaste el número!'.
    Correcciones: Se cambio la constante 'ATTEMPS' de 5 a 10 para coincidir el número de intentos solicitados.
                  Se cambio el mensaje a "!!!Pérdistes!!!".

    Prueba 6:
    Descripción de la prueba: El usuario adivina el numero antes de los 10 intentos.
    Resultado esperado: Se debe de mostrar el mensaje en color verde: "Felicitaciones! adivinaste el número!".
    Estado de la prueba: Insatisfactorio.
    Resultado obtenido: Muestra el mensaje en color negro: 'Incorrecto!'.
                        Aunque se ingrese el numero correcto, la condicional siempre marca false, ya que se hace la comparación del valor y del tipo de dato
                        ingresado que es tipo String, por lo que nunca va a coincidir.
    Correcciones: Se corrige el mensaje en color verde: 'Felicitaciones! adivinaste el número!'.
                  Se convierte el tipo de dato de 'userGuess' a Number para que pueda realizar correctamente la comparación.

    Prueba 7:
    Descripción de la prueba: El usuario selecciona la opción 'Comienza un nuevo juego' y se genera un nuevo número al azar.
    Resultado esperado: Se genera un nuevo al azar.
    Estado de la prueba: Insatisfactorio.
    Resultado obtenido: El numero al azar siempre es 1.
    Correcciones: Se corrige la fórmula para que genere un número del rango del 1 al 100.