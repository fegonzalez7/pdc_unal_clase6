# Programación de Computadores - UNAL
## Identificadores, variables y operadores
<table cellspacing="1" bgcolor="">
	<tr bgcolor="#252582">
		<th><b>Definición</b></th>
	</tr>
	<tr bgcolor="#e4e4ed">
		<td style="color:#141414">Un identificador es una secuencia de símbolos que se utilizan como nombres de variables, funciones, arreglos, clases y otras estructuras de los lenguajes de programación.</td>
	</tr>
</table>

Formas de escribir idenfificadores en Python:
 + secuencias de caracteres alfanuméricos del alfabeto inglés 
 + Usando ( _ ) *underscore* - *guión bajo*
 + No usar espacios
 + No usar caracteres especiales ($, &, *, #)
 + No iniciar con valores numéricos y de *preferencia* no incorporarlos 
 + NO ser una palabra reservada del lenguaje.

<div align='center'>
<figure> <img src="https://i.postimg.cc/KjrqrjZL/image.png" alt="" width="600" height="auto"/></br>
<figcaption><b>Palabras reservadas de Python</b></figcaption></figure>
</div>

<details><summary>Ejemplos de identificadores válidos</summary><p>
<table cellspacing="3" bgcolor="">
	<tr style="text-align: left; vertical-align: middle;" bgcolor="#">
		<th>
			<p align="left">
			  i<br>
        x<br> 
        n<br>
        suma<br>
        sumando1<br>
        sumando2<br>
        Edad<br>
        paisDeNacimiento<br>
        _nombre<br>
        area_circulo<br>
        false<br>
        Variable<br>
        snake_case<br>
        MACRO_CASE<br>
        camelCase<br>
        CapWords<br>
		</th>
	</tr>
</table>
</p></details><br>

<details><summary>Ejemplos de identificadores inválidos</summary><p>
<table cellspacing="3" bgcolor="">
	<tr style="text-align: left; vertical-align: middle;" bgcolor="#">
		<th>
			<p align="left">
        1er_mes<br>
        primer nombre<br>
        while<br>
        p@dre<br>
        día<br>
        velocidad-maxima<br>
        True<br>
        Var#1<br>
		</th>
	</tr>
</table>
</p></details><br>

## Casing
Es el uso de mayusculas y minusculas (así como otros caracteres). Python es *sensitive case*, lo que significa que distingue entre mayúculas y minúculas., *e.g.* No es o mismo variable a VARIABLE.

### Lowercase
Es el uso exclusivo de mínusculas.

### Uppercase
Es el uso exclusivo de mayusculas.

### Camelcase
Consiste en la capitalización de la inicial de cada palabra compuesta excepto la inicial. El cambio entre minúculas y mayúsculas se asemeja a las jorobas de un camello. 

Ejemplos: 
 + soyUnNumero
 + cantidadEstudiantesClase
 + letrasAlfabeto
 + sumaElementosInternos
 + linAlgebraDotProduct

 Esta notación se usa principalmente en C, C++, Java, JavaScript y hay un debate pero en Python también.

### Snakecase
Consite en el uso de *underscore* para separar las palabras en una entidad compuesta, la cual estará siempre en minúscula. Las secciones se asemejan a las partes de una serpiente (?.

Ejemplos: 
 + soy_un_numero
 + cantidad_estudiantes_clase
 + letras_alfabeto
 + suma_elementos_internos
 + lin_algebra_dot_product

  Esta notación se usa principalmente en Ruby, PHP y hay un debate pero en Python también.

Hay otra que se llama *kebab case*, así que revisen.

**Entonces,** cúal usar?....les recomiendo *camelcase*, aunque *snakecase* es aceptable también.

## Variables
<table cellspacing="1" bgcolor="">
	<tr bgcolor="#252582">
		<th><b>Definición</b></th>
	</tr>
	<tr bgcolor="#e4e4ed">
		<td style="color:#141414">Una variable es un espacio de memoria donde se almacena un dato, un espacio donde se guarda la información necesaria para realizar las acciones que ejecutan los programas.</td>
	</tr>
</table>

<div align='center'>
<figure> <img src="https://i.postimg.cc/zv3zzRDj/image.png" alt="" width="600" height="auto"/></br>
<figcaption><b>Representación física de una variable.</b></figcaption></figure>
</div>

### Variables en python
Para declarar una variable se necesitan principalmente dos componentes:
el nombre y el tipo de dato. 

```python
  nombre_variable : <tipo_dato>
```
### Tipado estático vs tipado dinámico
Ya que python es un lenguaje interpretado soporta tipado dinámico, esto es, para que un programa funcione *no* es necesario especificar el tipo de la variable, porque en tiempo de ejecución se va cambiando el espacio en memoria necesario para alojar la información. 

Para el programador esto se puede considerar algo *sencillo*, ya que solo decalra variables y el interprete hace el resto, sin embargo esto es una *mala práctica*. Por lectura, por eficicencia, por elegancia, es mejor hacer tipado estático, es decir especificar el tipo de variable, para reservar el espacio adecuado en memoria. La mayoría de lenguajes compilados usa tipado estático.

**Pro tip:** Una buena práctica de programación∗ es asignarle el nombre a una variable de tal manera que indique por un lado el papel que desempeña dicha variable en el algoritmo y por otro los posibles valores que almacena.

<div align='center'>
<figure> <img src="https://i.postimg.cc/hvbjvQHQ/image.png" alt="" width="600" height="auto"/></br>
<figcaption><b>Ejemplos de nombres para variables.</b></figcaption></figure>
</div>

## Tipos de datos
### Enteros
Si x es una variable algebraica que varia en el conjunto Z, para definir x
en el lenguaje Python se utiliza la expresión:

```python
  x : int
```
### Declarar vs Inicializar
**Declarar:** Consiste en nombrar la variable y *declarar* su tipo, sin especificar un valor inicial.

**Inicializar:** Consiste en dar un valor inicial luego de declarar una variable.

```python
# Declarar variable
x : int
# Inicializar variable
x = 10 
# Declarar e inicializar variable
x : int = 10
```
**Pro tip:** Para dar valor a una variable, se utiliza el operador de *asignación*, un = (signo igual). 

**Pro tip:** Para poner comentarios en el código de python se utiliza # (asterisco), todo lo que está comentado no será tenido en cuenta en el programa. Comentar es **FUNDAMENTAL** para entender el code. 

En Python no hay una distinción tan clara de la cantidad de espacio que usa un entero, en lenguajes como C se tienen `int8`, `uint16`, `long`, donde se especifican la cantidad de bits para almacenar la varible. Si se queire consultar la cantidad de bits y la representación binaria se puede usar.

```python
# Declarar e inicializar variable
x : int = 10
# Cantidad de bits
print(x.bit_length)
# Representacion binaria 
print(bin(x)) 
```
### Flotantes
Si x es una variable algebraica que varia en el conjunto R, para definir x
en el lenguaje Python se utiliza la expresión:

```python
  x : float
```

El subconjunto de los n´umeros reales que pueden ser representados en el lenguaje Python, es un subconjunto propio de los racionales, que se representan con 64 bits (8 bytes) y que usan un tipo de codificación definida por el IEEE standard for Binary Floating-Point Arithmetic 754 de 1985, los valores distintos de 0 de este conjunto varían en el rango:

$$−1.7976931348623157\cdot10^{+308} ≤ x ≤ −2.2250738585072014\cdot10^{−308}$$

y 

$$2.2250738585072014\cdot10^{−308} ≤ x ≤ 1.7976931348623157\cdot10^{+308}$$

Los n´umeros reales de máquina son finitos y por lo tanto, existen n´umeros
reales que no se pueden representar. Además, la mayoría de los n´umeros se acumulan alrededor del 0 y hacia los extremos superior e inferior se encuentran más dispersos.

Ejemplos de flotantes:
```python
e = 2.7182818284
gamma : float = 0.577215664901
phi = +1.61803398874989
X = -1.0
const_Boltzmann = 1.3806488E-23
Luz : float = 2.998e+8
Avogadro = +6.02214129e+23
G : float = 6.67384e-11
Plank = 6.62606896E-34
```

### Constantes
A diferencia de C, Java o Javascript, en Python no hay constantes perse, se suele declarar una variable global en *snake case* maúsculas para indicar que se trata de un valor persistente.

```python
MAIN_VALUE = 10
CONST_FREQ = 500.56 
```

### Booleanos
Si x es una variable algebraica que varia en el conjunto B, para definir x
en el lenguaje Python se utiliza la expresión:

```python
  x : bool
```

El conjunto de los booleanos tiene dos componentes: $$B = \{V,F\}$$

En python:
$$V\rightarrow True \ \ \ \ \ \ \ F\rightarrow False $$

Ejemplos de booleanos:
```python
b = True
flag: bool = True
exp = False
isPrime: bool = False
```

**Pro trip:** En Python la representación interna de los valores booleanos se hace mediante el uso de valores enteros int de 32 bits de la siguiente manera:
el valor lógico F se representa con el entero 0 (cero) y el valor lógico V se representa con cualquier entero distinto de 0, por costumbre se usa el entero 1 (uno). De lo anterior se obtienen las siguientes equivalencias lógicas:

$$True \Longleftrightarrow 1 \ \ \ \ \ \ \ \ False \Longleftrightarrow 0$$

### Caracteres y cadenas de caracteres
Un carácter es el elemento mínimo de información usado para representar,
controlar, transmitir y visualizar datos. Al conjunto de caracteres usados
con este fin se le llama Esquema de codificación. Los esquemas de
codificación en general usan un n´umero de bits o bytes fijos. Por ahora solo
consideraremos el ASCII. En Python son representados como cadenas de
caracteres de un sólo carácter.

<div align='center'>
<figure> <img src="https://i.postimg.cc/7hH1sGJ1/image.png" alt="" width="600" height="auto"/></br>
<figcaption><b>Tabla de caracteres con equivalente en ASCII.</b></figcaption></figure>
</div>

Código Estadounidense Estándar para el Intercambio de Información
(American Standard Code for Information Interchange):

 + En su versión original usa 7 bits, definiendo 128 caracteres.
 + En la versión extendida usa 8 bits (esto es 1 byte), definiendo 256 caracteres.
 + Es la base de los archivos de texto plano (o sin formato). 
 + Es el esquema base para la escritura de programas en casi todos los lenguajes de programación (incluido Python)

Las variables tipo caracter se definen usando comillas dobles ("") o sencillas ('').

Ejemplos:
```python
char1 = "a"
char2 = 'x'
```
Para convertir de caracter a ASCII se emplea la función *ord()* y para convertir de ASCII a caracter *chr()*.

```python
ord('a')
```

```python
chr(97)
```

### Cadenas de caracteres o Strings
Una **cadena de caracteres** *str* es una secuencia de cero o más caracteres. Una cadena de caracteres se delimita por el carácter ' o por el carácter ". Una cadena de caracteres es una estructura de datos **inmutable**, esto significa que no puede ser cambiada. 

 + 'ejemplo de cadena'
 + "Cadena con un tabulado \t y una nueva \n línea"
 + 'Cadena con un carácter unicode \u01F4 y una comilla doble"' 
 + "Cadena con una comilla simple \’, una comilla doble \" y una diagonal invertida \\" 
 + La cadena vacía "" o ''

**Pro tip:** Diferencia entre "" y '', en general se utiliza doble comilla en caso que el string contenga comillas sencillas.

## Operadores
Es la manera de establer relaciones (operaciones) entre los tipos de variables.

 + **Operadores infijos:** Se aplican entre los operandos.
 + **Operadores prefijos:** Se aplica antes del operando.
 + **Operadores sufijos:** Se aplica después del operando.

### Operadores aritméticos
Se aplican a los datos de tipo numérico (luego veremos que algunos se pueden sobrecargar a otras estructuras de datos).

 + **Suma:** Usa el simbolo (+) y obtiene la suma de dos o más valores.
```python
# Suma de dos numeros
4 + 1 # Entero + Entero = Entero
4.0 + 1 # Real + lo que sea = Real 
``` 
  + **Resta:** Usa el simbolo (-), representa la sustracción cuando está entre dos operandos (infijo) o la negación (cambio de signo) cuando predece al oeprando (prefijo).
```python
# Sustacción de dos numeros
4 - 1 # Entero - Entero = Entero
-1 # Cambio de signo
``` 
 + **Multiplicación:** Usa el simbolo (*) y obtiene el producto entre dos o más valores.
```python
# Producto de dos numeros
4 * 2.0 # Entero * Real = ?
``` 
 + **División:** Usa el símbolo (/) y retorna la división exacta.
 ```python
# División de dos numeros
4 / 2 # Entero / Entero = ?
4.0 / 2 # Real / Entero =?
4.0 / 0 # Tan tan tan
``` 
 + **División Entera:** Usa el símbolo (//) y retorna la parte entera de la división exacta.
 ```python
# División exactas de dos numeros
5 // 2 # Entero / Entero = ?
5.0 // 2 # Real / Entero =?
``` 
 + **Módulo:** Usa el símbolo (%) y retorna el residuo de la divisón entre dos números.
$$m \ \text{mod} \ n = r \Longrightarrow \frac{m}{n}=c+r$$
 ```python
# modulo entre dos números
10 % 2 # Entero % Entero = ?
5.0 % 2 # Real / Entero =?
``` 
 + **Potencia:** Usa el símbolo (**) y retorna elevar a una cierta potencia un operando. <b>Importante:</b> NO se usa el símbolo (^) -> Acento circunflejo (Hay gente que le dice el sombrerito...que falta de nivel).
 ```python
# potencias entre dos números
5**2 # Cuadrados
5**3 # Cubos
81**0.5 # Raíces
``` 
### Operadores de asignación
 + **Asignación:** Usa el simbolo (=). La parte de la izquierda que debe ser una variable. Sirve para almacenar un dato en una variable. Asigna el valor de evaluar la parte de la derecha a la variable de la parte de la izquierda.
 ```python
pi : float = 3.14169265
``` 
 + **Asignación con suma:** Usa el simbolo (+=). La parte de la izquierda debe ser una variable. Suma la evaluación de parte de la derecha con el valor almacenado en la variable definida en la parte de la izquierda y guarda el resultado en la variable de parte de la izquierda.
 ```python
x : int = 1
x += 1 # Equivalente a x = x + 1
``` 
Las asignaciones con operación no se pueden utilizar dentro de uan expresión (e.g. un ciclo), son operaciones en sí mismas.

 + **Asignación con resta:** Usa el simbolo (-=). La parte de la izquierda debe ser una variable. Resta al valor almacenado en la variable definida en la parte de la izquierda el resultado de la evaluación de parte de la derecha y guarda el resultado en la variable de parte de la izquierda.
 ```python
x : int = 2
x -= 1 # Equivalente a x = x - 1
``` 
 + **Asignación con multiplicación:** Usa el simbolo (*=). La parte de la izquierda debe ser una variable. Multiplica el valor almacenado en la variable definida en la parte de la izquierda con la evaluación de parte de la derecha y guarda el producto en la variable de parte de la izquierda.
 ```python
x : int = 4
x *= 3 # Equivalente a x = x * 3
``` 
 + **Asignación con división:** Usa el simbolo (/=). La parte de la izquierda debe ser una variable. Divide el valor almacenado en la variable definida en la parte de la izquierda entre el valor de la evaluación de la parte de la derecha y guarda el resultado en la variable de parte de la izquierda.
 ```python
x : int = 4
x /= 2 # Equivalente a x = x / 2
``` 
 + **Asignación con división entera:** Usa el simbolo (//=). La parte de la izquierda debe ser una variable. Divide de forma entera el valor almacenado en la variable definida en la parte de la izquierda entre el valor de la evaluación de la parte de la derecha y guarda el resultado entero en la variable de parte de la izquierda. 
 ```python
x : int = 8
x //= 4 # Equivalente a x = x // 4
``` 
 + **Asignación con residuo:** Usa el simbolo (%=). La parte de la izquierda debe ser una variable. Calcula el residuo de dividir el valor almacenado en la variable definida en la parte de la izquierda entre el valor de la evaluación de la parte de la derecha y guarda el resultado en la variable de parte de la izquierda.
 ```python
x : int = 8
x %= 4 # Equivalente a x = x % 4
``` 

**Ejemplo:** Calcular la fuerza de atracción entre la tierra y un cuerpo sobre su superficie. 
$$\text{Ley de la gravitación universal:} \ G=\frac{m_1 \cdot m_2}{r^2}$$

```python
G : float = 6.67384e-11 # Constante de Cavendish [Nm^2/kg^2]
m1 : float = 5.972e+24 # Masa de la Tierra [kg]
m2 : float = 58 # Masa de alguna victima
r : float = 6400e3 # Radio de la Tierra [m]
``` 

```python
# Solución 1
F = G * m1 * m2 / r * r
``` 
```python
# Solución 2
F = G * m1 * m2 / r^2
``` 
```python
# Solución 3
F = G * m1 * m2 / r**2
``` 
### Operadores lógicos
Permiten determinar juicios de valor sobre proposiciones lógicas, su resultando es un booleano.

 + **Igualdad:** Evalua si dos variables son iguales. Se usa el simbolo (==).
 $$ \alpha == \beta \Longleftrightarrow \alpha = \beta$$
 ```python
alpha : int = 10
beta : int = 10 
alpha == beta
 ```

 + **Diferencia:** Evalua si dos variables son diferentes. Se usa el simbolo (!=).
 $$\alpha\ != \beta \Longleftrightarrow \alpha \neq \beta$$
 ```python
alpha : int = 10
beta : int = 11 
alpha != beta
 ```

 + **Mayor estricto:** Evalua si la variable de la izquierda es mayor que la de la derecha. Se usa el simbolo (>).
 $$\alpha\ > \beta \Longleftrightarrow \alpha > \beta$$
 ```python
alpha : int = 10
beta : int = 11 
alpha > beta
 ```

 + **Menor estricto:**  Evalua si la variable de la izquierda es menor que la de la derecha. Se usa el simbolo (<).
 $$\alpha\ < \beta \Longleftrightarrow \alpha < \beta$$
 ```python
alpha : int = 10
beta : int = 11 
alpha < beta
 ```

  + **Mayor igual:**  Evalua si la variable de la izquierda es mayor o igual  que la de la derecha. Se usa el simbolo (>=).
 $$\alpha\ >= \beta \Longleftrightarrow \alpha \geq \beta$$
 ```python
alpha : int = 10
beta : int = 10 
alpha >= beta
 ```

  + **Menor igual:** Evalua si la variable de la izquierda es menor o igual  que la de la derecha. Se usa el simbolo (<=).
 $$\alpha\ <= \beta \Longleftrightarrow \alpha \leq \beta$$
 ```python
alpha : int = 9
beta : int = 10 
alpha <= beta
 ```
### Operadores relacionales
Permiten aplicar operaciones boolenas (no se preocupen en Digital lo van a ver en detalle), en general es evaluar juicios de valor compuestos.

  + **Conjunción/AND:** Permite evaluar la operación *and* (y en español). Se utiliza la palabra reservada *and*.
<table cellspacing="1" bgcolor="">
	<tr bgcolor="#252582">
		<th><b>A</b></th>
    <th><b>B</b></th>
    <th><b>AND(A,B)</b></th>
	</tr>
	<tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
		<td style="color:#141414">0</td>
    <td style="color:#141414">0</td>
    <td style="color:#141414">0</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
		<td style="color:#141414">0</td>
    <td style="color:#141414">1</td>
    <td style="color:#141414">0</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
		<td style="color:#141414">1</td>
    <td style="color:#141414">0</td>
    <td style="color:#141414">0</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
		<td style="color:#141414">1</td>
    <td style="color:#141414">1</td>
    <td style="color:#141414">1</td>
	</tr>
</table>

 ```python
1 and 0 
True and False
 ```
**Pro tip:** Los que hayan programado en otros lenguajes sabran que el simbolo & (ampersand) representa la operación AND, pero en Python es a un nivel binario, esto es si se aplica con valores numéricos, estos se transformarán a bits y se aplicará la operación.

   + **Disyunción/OR:** Permite evaluar la operación *or* (o en español). Se utiliza la palabra reservada *or*.

<table cellspacing="1" bgcolor="">
	<tr bgcolor="#252582">
		<th><b>A</b></th>
    <th><b>B</b></th>
    <th><b>OR(A,B)</b></th>
	</tr>
	<tr tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
		<td style="color:#141414">0</td>
    <td style="color:#141414">0</td>
    <td style="color:#141414">0</td>
	</tr>
  <tr tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
		<td style="color:#141414">0</td>
    <td style="color:#141414">1</td>
    <td style="color:#141414">1</td>
	</tr>
  <tr tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
		<td style="color:#141414">1</td>
    <td style="color:#141414">0</td>
    <td style="color:#141414">1</td>
	</tr>
  <tr tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
		<td style="color:#141414">1</td>
    <td style="color:#141414">1</td>
    <td style="color:#141414">1</td>
	</tr>
</table>

 ```python
1 or 0 
True or False
 ```

**Pro tip:** Los que hayan programado en otros lenguajes sabran que el simbolo | (vertical line) representa la operación OR, pero en Python es a un nivel binario, esto es si se aplica con valores numéricos, estos se transformarán a bits y se aplicará la operación.

  + **Negación/NOT:** Permite evaluar la operación *not*. Se utiliza la palabra reservada *not*.
<table cellspacing="1" bgcolor="">
	<tr bgcolor="#252582">
		<th><b>A</b></th>
    <th><b>NOT(A)</b></th>
	</tr>
	<tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
		<td style="color:#141414">0</td>
    <td style="color:#141414">1</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">1</td>
    <td style="color:#141414">0</td>
	</tr>
</table>

 ```python
not 0
not False
 ```

**Pro tip:** Los que hayan programado en otros lenguajes sabran que el simbolo ~ (virgulilla) representa la operación NOT, pero en Python es a un nivel binario, esto es si se aplica con valores numéricos, estos se transformarán a bits y se aplicará la operación.

**Ejemplo:** Establecer la relación lógica que permita determinar si un una pareja ordenada `(a,b)` pertenece al conjunto `[-2,3.5) x (-1.25,1.5] U {(x,y):x^2+y^2 <= 1}`.
<div align='center'>
<figure> <img src="https://i.postimg.cc/P5gt8gwk/image.png" alt="" width="500" height="auto"/></br>
<figcaption><b></b></figcaption></figure>
</div>

```python
# Lo que está dentro del rectangulo
a > -2 and a <= 3.5
b >= -1.5 and b < 1.5
# Lo que está fuera del ciculo
a * a + b * b >= 1
# Uniendo los dos conjuntos
(a > -2 and a <= 3.5 and b >= -1.5 and b < 1.5) and (a * a + b * b >= 1)
```

### Precedencia de opearaciones
En la siguiente tabla se presenta la prioridad de los principales operadores
de Python, la prioridad más alta es la 1 y la más baja es la 9. Si dos operaciones tienen la misma prioridad se resuelve de izquierda a derecha.

<table cellspacing="1" bgcolor="">
	<tr style="text-align: center; vertical-align: middle;" bgcolor="#252582">
		<th><p align=center><b>Operador(es)</b></p></th>
    <th><b>Prioridad</b></th>
	</tr>
	<tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
		<td style="color:#141414">()</td>
    <td style="color:#141414">1</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">not &nbsp &nbsp &nbsp -(signo menos) &nbsp &nbsp &nbsp +(signo más) &nbsp &nbsp &nbsp **(potencia)</td>
    <td style="color:#141414">2</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">* &nbsp &nbsp &nbsp / &nbsp &nbsp &nbsp // &nbsp &nbsp &nbsp %</td>
    <td style="color:#141414">3</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">+ &nbsp &nbsp &nbsp -</td>
    <td style="color:#141414">4</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">< &nbsp &nbsp &nbsp > &nbsp &nbsp &nbsp <= &nbsp &nbsp &nbsp >=</td>
    <td style="color:#141414">5</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">== &nbsp &nbsp &nbsp ~=</td>
    <td style="color:#141414">6</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">and</td>
    <td style="color:#141414">7</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">or</td>
    <td style="color:#141414">8</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">= &nbsp &nbsp &nbsp += &nbsp &nbsp &nbsp -= &nbsp &nbsp &nbsp *= &nbsp &nbsp &nbsp /= &nbsp &nbsp &nbsp //= &nbsp &nbsp &nbsp %=</td>
    <td style="color:#141414">9</td>
	</tr>
</table>

**Ejemplos:**
1. Resolver la experesión `42 // 6 + 7 * 3 - 39` y determinar el orden de cada operación.

```python
42 // 6 + 7 * 3 - 39
# // y * prioridad 3
# + y  - prioridad 4
# 42 // 6 + 7 * 3 - 39 -> (((42 // 6) + (7 * 3)) - 39)
# Paso 1
42 // 6 # Resultado 7
# Paso 2 
7 * 3 # Resultado 21
# Paso 3
7 + 21 - 39  # Resultado -11
```

2. Resolver la experesión `12.0 * 3 - -4.0 + 8 // 2 % 3` y determinar el orden de cada operación.

```python
12.0 * 3 - -4.0 + 8 // 2 % 3
# -(signo menos) prioridad 2
# *, //, y % prioridad 3
# - y + prioridad 4
# 12.0 * 3 - -4.0 + 8 // 2 % 3 -> (((12.0 * 3) - (-4.0)) + ((8 // 2) % 3))
# Paso 1
-(-4.0) # Resultado +4.0
# Paso 2 
12.0 * 3 # Resultado 36.0
# Paso 3
8 // 2 # Resultado 4
# Paso 4
4 % 3 # Resultado 1
# Paso 5
36.0 + 4.0 + 1 # Resultado 41.0
```

3. Resolver la experesión `(-2 + 5 % 3 * 4) // 4 + 2` y determinar el orden de cada operación.

```python
(-2 + 5 % 3 * 4) // 4 + 2 # Resultado 3.0
```

