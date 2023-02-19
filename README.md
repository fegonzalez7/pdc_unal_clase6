# Programación de Computadores - UNAL
## Identificadores y variables
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
