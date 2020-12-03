# Sistemas_En_Tiempo_Real

Una caja fuerte es una herramienta para guardar objetos de valor, pues hoy día se utiliza con mayor frecuencia para evitar su posible pérdida o inesperadamente un robo cuando no está en su lugar de residencia. Para ello decidimos implementar algo similar utilizando un microcontrolador STM32L476RG Nucleo-64 donde se implementó una caja fuerte, utilizando el programa STM32cubeIDE se creó su programa utilizando el lenguaje C.

# MATERIALES PARA REALIZAR LA CAJA FUERTE.

-STM32L476RG Nucleo-64

-cable para conectar el STM32L476RG Nucleo-64

-Instalación del programa STM32cubeIDE (https://unalman.gitbook.io/estructuras-computacionales/instalacion-stm32cubeide)

-teclado matricial 4x4

-pantalla LCD keipad shield de (16x2).

-2 leds (rojo y verde) "para indicar cuando está cerrado y abierto.

una vez identificado los tópicos a tener en cuenta, se dispuso a crear el código, para ello utilizamos un teclado matricial  4x4 para ingresar su contraseña y con un botón de confirmación para que lea la contraseña ingresada, un par de leds que funcionan como indicadores cuando se abre y se cierra la caja fuerte y su pantalla lcd para ver el registro de la contraseña ingresada. Cabe aclarar que la contraseña para ingresar a la caja fuerte es el código "2017" y su botón de confirmación es " * " por el momento la contraseña solamente se puede cambiar desde el código del programa de STM32cubeIDE.
Cuando se ingresa una contraseña diferente, la caja fuerte sigue cerrada y solo se abrirá cuando ingresen la contraseña correcta.

En este ejemplo encontraran implementado máquinas de estado y para la culminación con éxito de la asignatura sistemas en tiempo real la implementación en sistemas operativos.

# Diagrama de Flujo "caja fuerte"

![Diagrama de Flujo caja fuerte](/diaframa%20de%20flujo.JPG?raw=true "Diagrama de Flujo caja fuerte")  


# Explicación:

Después de iniciar nuestra variable input con un valor diferente a cero, este va a recibir el valor que genera el teclado matricial 4x4, en la pantalla LCD keipad shield de (16x2) mostrara un mensaje de "Bienvenido" y "ingrese pin", al mostrarlo por pantalla el usuario oprime un valor del teclado el cual se guarda en input, pasa a "contras_ciclo" que va ser el valor que lo lee y generara el ciclo de verificación y "cursor" es el que se va a encargarse de imprimirlo y de ir acumulando cada carácter de la contraseña ingresada por el usuario, en el rombo de condicional se mira si los valores ingresados son igual o mayor a 4, si el valor ingresado es menor a 4 o no es correcto, la caja fuerte seguirá bloqueada, mostrara un mensaje de "Error" y el usuario debe volver a ingresar la contraseña, cuando es el caso contrario en donde la contraseña ingresada corresponde a 4 caracteres y es correcta, entonces la caja fuerte se abrirá y mostrara en este caso "Abierto" el cual corresponde al valor de "pulsa" en el código.

En esta imagen podemos observar cuando se le pide al usuario que: "ingrese pin"

![Bienvenido_ingresepin](https://github.com/fredymendezbustamante/Sistemas-en-Tiempo-Real/blob/main/Bienvenido_ingresepin.jpeg?raw=true "Optional Title") 

En esta imagen podemos observar que esta encendido el led, rojo el cual indica que la caja fuerte está cerrada.

![Led_Rojo](https://github.com/fredymendezbustamante/Sistemas-en-Tiempo-Real/blob/main/Led_Rojo.jpeg?raw=true "Optional Title")


En esta imagen podemos observar que esta encendido el led, ver el cual indica que la caja fuerte está abierta.

![Led_Verde](https://github.com/fredymendezbustamante/Sistemas-en-Tiempo-Real/blob/main/Led_Verde.jpeg?raw=true "Optional Title")


# Funcionamiento de la caja fuerte.
![Caja_fuerte](https://github.com/fredymendezbustamante/Sistemas-en-Tiempo-Real/blob/main/Caja_fuerte.gif?raw=true)



