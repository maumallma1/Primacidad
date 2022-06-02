<h1>GENERADOR DE NúMEROS PRIMOS SEGÚN CANTIDAD DE BITS</h1>
<h2>Introducción</h2>
El programa que implementamos busca generar 10 números primos, según la cantidad de primos que le coloquemos, en esta ocasión probaremos con los valores de 16, 32 y 64 bits. Estos números primos serán diferentes entre sí y cumplirán el rango de tener en su MSB y LSB el bit 1, otorgandonos un número que sea siempre impar y que ocupe la cantidad de bits que solicitamos.<br>
(Es necesario leer el README anterior, dado el programa requiere de funciones antes mencionadas).
<h2>Implementaciones nuevas en el código</h2>
<h3>1. Función Randombits</h3>
Tiene por finalidad crear un número impar de b cantidad de bits, el cual se usará mas adelante para generar números primos.<br>
![image](https://user-images.githubusercontent.com/85748915/171537351-cbfc019c-f521-47cb-ae85-ce287af9524e.png)
<br>
- Tiene por único parámetro el entero b.
- La variable po, almacena el valor de 2^b, el cual será el delimitador del generador de primos más adelante.
- La variable pos, almacena el valor de 2^(b-1) el cual se usara para crear una variable que funcionará como máscara de números primos mas adelante.
- La variable "n", almacenará un número aleatorio entre 0 y "po".
- La variable "m", será la máscara para filtrar este número "n".
- Al final a n le aplicaremos la máscara m mediante un or lógico, asi filtraremos un número impar que cumpla con la cantidad de bits que tiene "b".
<h3>2. Función Randomgen</h3>
Tiene por finalidad generar números primos, usando como número base al resultado de la función Randombits, para luego aplicarle el Test de Miller, el cual nos devolverá, mediante un bucle, nos devolverá un número que pase el test, es decir que sea primo.<br>
![image](https://user-images.githubusercontent.com/85748915/171540460-81c25080-0ee9-4cdb-8695-c6792158afde.png)
<br>
- Tiene por único parámetro el entero b.
- La variable n, almacenará el número impar resultante de la función Randombits.
- Luego procederá a crear un bucle condicional while, con la condición que mientras el Test de Miller de n sea falso, entonces ese número sea aumentado en 2.
- Así comenzaremos a incrementar el número impar de 2 en 2, hasta encontrar un número que si cumpla el Test de Miller, es decir, que sea primo.
<h3>3. Funcionamiento</h3>
<h4>De 16 bits</h4>
![image](https://user-images.githubusercontent.com/85748915/171542340-e67b297f-9475-4886-a1d8-d9815a54b885.png)
<br>
![image](https://user-images.githubusercontent.com/85748915/171542640-7b68b77d-46a6-4c5c-ba92-3517c8c028f9.png)
<br>
<h4>De 32 bits</h4>
![image](https://user-images.githubusercontent.com/85748915/171543049-debed7c8-83a2-4dd7-a21f-c2aec1afebf3.png)
<br>
![image](https://user-images.githubusercontent.com/85748915/171542863-72094d09-e62f-48d3-903d-a74e27dacfa7.png)
<br>
<h4>De 64 bits</h4>
![image](https://user-images.githubusercontent.com/85748915/171542931-475e3e0d-37c5-4f76-98c1-383e96afeeef.png)
<br>
![image](https://user-images.githubusercontent.com/85748915/171543095-1b75e212-5522-48b9-a501-fefb979dd9ab.png)

<br>
