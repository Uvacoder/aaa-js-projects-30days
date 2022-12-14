<div align="center">
  <h1> 30 D铆as de JavaScript: Funciones</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/asabeneh?style=social">
  </a>

<sub>Autor:
<a href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br>
<small> Enero, 2020</small>
</sub>

</div>

[<< D铆a 6](../dia_06_Bucles/dia_06_bucles.md) | [D铆a 8 >>](../dia_08_Objetos/dia_08_objetos.md)

![Thirty Days Of JavaScript](../images/banners/day_1_7.png)

- [馃摂 D铆a 7](#馃摂-d铆a-7)
  - [Funciones](#funciones)
    - [Funci贸n declarativa](#funci贸n-declarativa)
    - [Funci贸n sin par谩metros y return](#funci贸n-sin-par谩metros-y-return)
    - [Funci贸n que retorna un valor](#funci贸n-que-retorna-un-valor)
    - [Funci贸n con un par谩metro](#funci贸n-con-un-par谩metro)
    - [Funci贸n con dos par谩metros](#funci贸n-con-dos-par谩metros)
    - [Funci贸n con muchos par谩metros](#funci贸n-con-muchos-par谩metros)
    - [Funci贸n con n煤mero ilimitado de par谩metros](#funci贸n-con-n煤mero-ilimitado-de-par谩metros)
      - [N煤mero ilimitado de par谩metros en una funci贸n regular](#n煤mero-ilimitado-de-par谩metros-en-una-funci贸n-regular)
      - [N煤mero ilimitado de par谩metros en una funci贸n flecha](#n煤mero-ilimitado-de-par谩metros-en-una-funci贸n-flecha)
    - [Funci贸n an贸nima](#funci贸n-an贸nima)
    - [Funci贸n de expresi贸n](#funci贸n-de-expresi贸n)
    - [Funciones de autoinvocaci贸n](#funci贸n-de-autoinvocaci贸n)
    - [Funci贸n flecha](#funci贸n-flecha)
    - [Funci贸n con par谩metros por defecto](#funci贸n-con-par谩metros-por-defecto)
    - [Funci贸n declarativa versus funci贸n flecha](#funci贸n-declarativa-versus-funci贸n-flecha)
  - [馃捇 Ejercicios](#馃捇-ejercicios)
    - [Ejercicios: Nivel 1](#ejercicios-nivel-1)
    - [Ejercicios: Nivel 2](#ejercicios-nivel-2)
    - [Ejercicios: Nivel 3](#ejercicios-nivel-3)

# 馃摂 D铆a 7

## Funciones

Hasta ahora hemos visto muchas funciones JavaScript integradas. En esta secci贸n, nos centraremos en las funciones personalizadas. 驴Qu茅 es una funci贸n? Antes de comenzar a hacer funciones, comprendamos 驴Qu茅 es una funci贸n? y 驴Por qu茅 necesitamos una funci贸n?

Una funci贸n es un bloque reutilizable de c贸digo o declaraciones de programaci贸n dise帽adas para realizar una determinada tarea.

Una funci贸n se declara mediante la palabra clave function seguida de un nombre, seguido de par茅ntesis (). Un par茅ntesis puede tomar un par谩metro. Si una funci贸n toma un par谩metro, se llamar谩 con un argumento. Una funci贸n tambi茅n puede tomar un par谩metro predeterminado. Para almacenar datos en una funci贸n, una funci贸n debe devolver ciertos tipos de datos. Para obtener el valor llamamos o invocamos a la funci贸n.

La funci贸n hace c贸digo:

- limpio y f谩cil de leer
- reutilizable
- f谩cil de probar

Una funci贸n se puede declarar o crear de un par de maneras:

- _Funci贸n declarativa_
- _Funci贸n de expresi贸n_
- _Funci贸n anonima_
- _Funci贸n flecha_

### Funci贸n declarativa

Veamos c贸mo declaramos una funci贸n y c贸mo llamar a una funci贸n.

```js
//declaramos una funci贸n sin un par谩metro
function functionName() {
  // el c贸digo va aqu铆
}
functionName(); // llamando a la funci贸n por su nombre con par茅ntesis
```

### Funci贸n sin par谩metros y return

La funci贸n se puede declarar sin un par谩metro.

**Ejemplo:**

```js
// funci贸n sin par谩metros. La funci贸n eleva al cuadrado un n煤mero
function square() {
  let num = 2;
  let sq = num * num;
  console.log(sq);
}

square(); // 4

// funci贸n sin par谩metro
function addTwoNumbers() {
  let numOne = 10;
  let numTwo = 20;
  let sum = numOne + numTwo;

  console.log(sum);
}

addTwoNumbers(); // una funci贸n tiene que ser llamada por su nombre para ser ejecutada
```

```js
function printFullName() {
  let firstName = "Asabeneh";
  let lastName = "Yetayeh";
  let space = " ";
  let fullName = firstName + space + lastName;
  console.log(fullName);
}

printFullName(); // llamando a una funci贸n
```

### Funci贸n que retorna un valor

La funci贸n tambi茅n puede devolver valores, si una funci贸n no devuelve valores, el valor de la funci贸n no est谩 definido. Escribamos las funciones anteriores con return. A partir de ahora, retornaremos el valor a una funci贸n en lugar de imprimirlo.

```js
function printFullName() {
  let firstName = "Asabeneh";
  let lastName = "Yetayeh";
  let space = " ";
  let fullName = firstName + space + lastName;
  return fullName;
}
console.log(printFullName());
```

```js
function addTwoNumbers() {
  let numOne = 2;
  let numTwo = 3;
  let total = numOne + numTwo;
  return total;
}

console.log(addTwoNumbers());
```

### Funci贸n con un par谩metro

En una funci贸n podemos pasar diferentes tipos de datos(number, string, boolean, object, function) como un par谩metro.

```js
// funci贸n con un par谩metro
function functionName(parm1) {
  //el c贸digo va aqu铆
}
functionName(parm1); // durante la llamada o la invocaci贸n es necesario un argumento

function areaOfCircle(r) {
  let area = Math.PI * r * r;
  return area;
}

console.log(areaOfCircle(10)); // debe ser llamado con un argumento

function square(number) {
  return number * number;
}

console.log(square(10));
```

### Funci贸n con dos par谩metros

```js
// funci贸n con dos par谩metros
function functionName(parm1, parm2) {
  //el c贸digo va aqu铆
}
functionName(parm1, parm2); // durante la llamada o invocaci贸n se necesitan dos argumentos
// la funci贸n sin par谩metros no recibe entrada, as铆 que hagamos una funci贸n con par谩metros
function sumTwoNumbers(numOne, numTwo) {
  let sum = numOne + numTwo;
  console.log(sum);
}
sumTwoNumbers(10, 20); // llamando a la funci贸n
// si una funci贸n no es retorna esta no almacena datos, por lo que debe retornar

function sumTwoNumbers(numOne, numTwo) {
  let sum = numOne + numTwo;
  return sum;
}

console.log(sumTwoNumbers(10, 20));
function printFullName(firstName, lastName) {
  return `${firstName} ${lastName}`;
}
console.log(printFullName("Asabeneh", "Yetayeh"));
```

### Funci贸n con muchos par谩metros

```js
// funci贸n con m煤ltiples par谩metros
function functionName(parm1, parm2, parm3,...){
  //el c贸digo va aqu铆
}
functionName(parm1,parm2,parm3,...) // durante la llamada o la invocaci贸n necesita tres argumentos


// esta funci贸n toma un array como un par谩metro y suma los n煤meros en el array
function sumArrayValues(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum = sum + arr[i];
  }
  return sum;
}
const numbers = [1, 2, 3, 4, 5];
    //llamada a la funci贸n
console.log(sumArrayValues(numbers));


    const areaOfCircle = (radius) => {
      let area = Math.PI * radius * radius;
      return area;
    }
console.log(areaOfCircle(10))

```

### Funci贸n con n煤mero ilimitado de par谩metros

A veces no sabemos cu谩ntos argumentos va a pasar el usuario. Por lo tanto, debemos saber c贸mo escribir una funci贸n que pueda tomar un n煤mero ilimitado de argumentos. La forma en que lo hacemos tiene una diferencia significativa entre una funci贸n declarativa (funci贸n regular) y una funci贸n flecha. Veamos ejemplos tanto en la funci贸n declarativa como en la funci贸n flecha.

#### N煤mero ilimitado de par谩metros en una funci贸n regular

Una funci贸n declarativa proporciona una funci贸n con alcance de argumentos array como objeto. Se puede acceder a cualquier cosa que pasemos como argumento en la funci贸n desde el objeto de argumentos dentro de las funciones. Veamos un ejemplo

```js
// Accedemos a los argumentos del objeto
鈥?
function sumAllNums() {
 console.log(arguments)
}

sumAllNums(1, 2, 3, 4)
// Arguments(4)聽[1, 2, 3, 4, callee: 茠, Symbol(Symbol.iterator): 茠]

```

```js
// declaraci贸n
鈥?
function sumAllNums() {
  let sum = 0
  for (let i = 0; i < arguments.length; i++) {
    sum += arguments[i]
  }
  return sum
}

console.log(sumAllNums(1, 2, 3, 4)) // 10
console.log(sumAllNums(10, 20, 13, 40, 10))  // 93
console.log(sumAllNums(15, 20, 30, 25, 10, 33, 40))  // 173
```

#### N煤mero ilimitado de par谩metros en una funci贸n flecha

La funci贸n flecha no tiene el objeto de alcance de los argumentos
Para implementar una funci贸n que toma un n煤mero ilimitado de argumentos en una funci贸n de flecha, usamos el operador de propagaci贸n seguido de cualquier nombre de par谩metro. Se puede acceder a cualquier elemento que hayamos pasado como argumento en la funci贸n como array en la funci贸n de flecha. Veamos un ejemplo

```js
// Accedemos a los argumentos del objeto
鈥?
const sumAllNums = (...args) => {
 // console.log(arguments), objeto de argumentos no encontrado en la funci贸n flecha
 // en su lugar, usamos un par谩metro seguido de un operador de propagaci贸n (...)
 console.log(args)
}

sumAllNums(1, 2, 3, 4)
// [1, 2, 3, 4]

```

```js
// declaraci贸n
鈥?
const sumAllNums = (...args) => {
  let sum = 0
  for (const element of args) {
    sum += element
  }
  return sum
}

console.log(sumAllNums(1, 2, 3, 4)) // 10
console.log(sumAllNums(10, 20, 13, 40, 10))  // 93
console.log(sumAllNums(15, 20, 30, 25, 10, 33, 40))  // 173
```

### Funci贸n an贸nima

Funci贸n an贸nima o sin nombre

```js
const anonymousFun = function () {
  console.log("Soy una funci贸n an贸nima y mi valor se almacena en anonymousFun");
};
```

### Funci贸n de expresi贸n

Las funciones de expresi贸n son funciones an贸nimas. Despu茅s creamos una funci贸n sin nombre y la asignamos a una variable. Para retornar un valor de la funci贸n debemos llamar a la variable. Mira el ejemplo de abajo.

```js
// Function expression
const square = function (n) {
  return n * n;
};

console.log(square(2)); // -> 4
```

### Funci贸n de autoinvocaci贸n

Las funciones de autoinvocaci贸n son funciones an贸nimas que no necesitan ser llamadas para devolver un valor.

```js
(function (n) {
  console.log(n * n);
})(2); // 4, pero en lugar de solo imprimir si queremos regresar y almacenar los datos, hacemos lo que se muestra a continuaci贸n

let squaredNum = (function (n) {
  return n * n;
})(10);

console.log(squaredNum);
```

### Funci贸n flecha

La funci贸n flecha es una alternativa para escribir una funci贸n, sin embargo, la funci贸n declarativa y la funci贸n flecha tienen algunas diferencias menores.

La funci贸n flecha usa una flecha en lugar de la palabra clave _function_ para declarar una funci贸n. Veamos tanto la funci贸n declarativa como la funci贸n flecha.

```js
// As铆 es como escribimos una funci贸n normal o declarativa
// Cambiemos esta funci贸n de declarativa a una funci贸n flecha
function square(n) {
  return n * n;
}

console.log(square(2)); // 4

const square = (n) => {
  return n * n;
};

console.log(square(2)); // -> 4

// si tenemos solo una l铆nea en el bloque de c贸digo, se puede escribir de la siguiente manera, return expl铆cito
const square = (n) => n * n; // -> 4
```

```js
const changeToUpperCase = (arr) => {
  const newArr = [];
  for (const element of arr) {
    newArr.push(element.toUpperCase());
  }
  return newArr;
};

const countries = ["Finland", "Sweden", "Norway", "Denmark", "Iceland"];
console.log(changeToUpperCase(countries));

// ["FINLAND", "SWEDEN", "NORWAY", "DENMARK", "ICELAND"]
```

```js
const printFullName = (firstName, lastName) => {
  return `${firstName} ${lastName}`;
};

console.log(printFullName("Asabeneh", "Yetayeh"));
```

La funci贸n anterior solo tiene la declaraci贸n de return, por lo tanto, podemos retornar expl铆citamente de la siguiente manera.

```js
const printFullName = (firstName, lastName) => `${firstName} ${lastName}`;

console.log(printFullName("Asabeneh", "Yetayeh"));
```

### Funci贸n con par谩metros por defecto

A veces, pasamos valores predeterminados a los par谩metros, cuando invocamos la funci贸n, si no pasamos un argumento, se usar谩 el valor predeterminado. Tanto la funci贸n declarativa como la funci贸n flecha pueden tener un valor o valores predeterminados.

```js
// sintaxis
// Declarando una funci贸n
function functionName(param = value) {
  //c贸digo
}

// Llamando una funci贸n
functionName();
functionName(arg);
```

**Example:**

```js
function greetings(name = "Peter") {
  let message = `${name}, welcome to 30 Days Of JavaScript!`;
  return message;
}

console.log(greetings());
console.log(greetings("Asabeneh"));
```

```js
function generateFullName(firstName = "Asabeneh", lastName = "Yetayeh") {
  let space = " ";
  let fullName = firstName + space + lastName;
  return fullName;
}

console.log(generateFullName());
console.log(generateFullName("David", "Smith"));
```

```js
function calculateAge(birthYear, currentYear = 2019) {
  let age = currentYear - birthYear;
  return age;
}

console.log("Age: ", calculateAge(1819));
```

```js
function weightOfObject(mass, gravity = 9.81) {
  let weight = mass * gravity + " N"; // el valor tiene que ser cambiado a string primero
  return weight;
}

console.log("Weight of an object in Newton: ", weightOfObject(100)); // 9.81 es la gravedad en la superficie de la tierra
console.log("Weight of an object in Newton: ", weightOfObject(100, 1.62)); // gravedad en la superficie de la luna
```

Veamos c贸mo escribimos las funciones anteriores con funciones flecha.

```js
// sintaxis
// declarando una funci贸n
const functionName = (param = value) => {
  //c贸digo
};

// Llamando a la  funci贸n
functionName();
functionName(arg);
```

**Example:**

```js
const greetings = (name = "Peter") => {
  let message = name + ", welcome to 30 Days Of JavaScript!";
  return message;
};

console.log(greetings());
console.log(greetings("Asabeneh"));
```

```js
const generateFullName = (firstName = "Asabeneh", lastName = "Yetayeh") => {
  let space = " ";
  let fullName = firstName + space + lastName;
  return fullName;
};

console.log(generateFullName());
console.log(generateFullName("David", "Smith"));
```

```js
const calculateAge = (birthYear, currentYear = 2019) => currentYear - birthYear;
console.log("Age: ", calculateAge(1819));
```

```js
const weightOfObject = (mass, gravity = 9.81) => mass * gravity + " N";

console.log("Weight of an object in Newton: ", weightOfObject(100)); // 9.81 es la gravedad en la superficie de la tierra
console.log("Weight of an object in Newton: ", weightOfObject(100, 1.62)); // gravedad en la superficie de la luna
```

### Funci贸n declarativa versus funci贸n flecha

Ser谩 cubierto en otra secci贸n.

馃寱 Tienes una energ铆a ilimitada. Acabas de completar los desaf铆os del d铆a 7 y llevas siete pasos de tu camino hacia la grandeza. Ahora haz algunos ejercicios para tu cerebro y tus m煤sculos.

## 馃捇 Ejercicios

### Ejercicios: Nivel 1

1. Declare una funci贸n _fullName_ e imprima su nombre completo.
2. Declare una funci贸n _fullName_ y ahora toma firstName, lastName como par谩metro y retorna su nombre completo.
3. Declare una funci贸n _addNumbers_ que toma dos par谩metros y retorna la suma de ambos.
4. El 谩rea de un rect谩ngulo se calcula de la siguiente manera: _area = length x width_. Escribe una funci贸n _areaOfRectangle_ que calcule el 谩rea de un rect谩ngulo.
5. El per铆metro de un rect谩ngulo se calcula de la siguiente manera: _perimeter= 2x(length + width)_. Escribe una funci贸n _perimeterOfRectangle_ que calcule el per铆metro de un rect谩ngulo.
6. El volumen de un prisma rectangular se calcula de la siguiente manera: _volume = length x width x height_. Escribe una funci贸n _volumeOfRectPrism_ que calcule el volumen de un prisma.
7. El 谩rea de un c铆rculo se calcula de la siguiente manera: _area = 蟺 x r x r_. Escribe una funci贸n _areaOfCircle_ que calcule el 谩rea de un c铆rculo.
8. La circunferencia de un c铆rculo se calcula de la siguiente manera: _circumference = 2蟺r_. Escribe una funci贸n _circumOfCircle_ que calcule la circunferencia de un c铆rculo.
9. La densidad de una sustancia se calcula de la siguiente manera:_density= mass/volume_. Escribe una funci贸n _density_ que calcule la densidad de una sustancia.
10. La velocidad se calcula dividiendo el total de la distancia recorrida por un objeto en movimiento entre el tiempo total. Escribe una funci贸n que calcule la velocidad de un objeto en movimiento, _speed_.
11. El peso de una sustancia se calcula de la siguiente manera: _weight = mass x gravity_. Escribe una funci贸n _weight_ que calcule el peso de una sustancia.
12. La temperatura en 掳C se puede convertir a 掳F usando esta f贸rmula: _掳F = (掳C x 9/5) + 32_. Escribe una funci贸n _convertCelsiusToFahrenheit_ que convierta 掳C a 掳F.
13. El 铆ndice de masa corporal (IMC) se calcula de la siguiente manera: _imc = peso en Kg / (altura x altura) en m2_. Escribe una funci贸n que calcule _imc_. El IMC se utiliza para definir de forma amplia diferentes grupos de peso en adultos de 20 a帽os o m谩s. Compruebe si una persona tiene un _peso bajo, peso normal, con sobrepeso_ u _obeso_ seg煤n la informaci贸n que se proporciona a continuaci贸n.

    - Se aplican los mismos par谩metros de grupos tanto a hombres como a mujeres.
    - _Peso bajo_: IMC inferior a 18,5
    - _Peso normal_: IMC de 18,5 a 24,9
    - _Sobrepeso_: IMC de 25 a 29,9
    - _Obeso_: IMC es 30 o m谩s

14. Escribe una funci贸n llamada _checkSeason_, toma un par谩metro de mes y retorna la estaci贸n: Oto帽o, Invierno, Primavera o Verano.
15. Math.max retorna su argumento m谩s grande. Escriba una funci贸n findMax que tome tres argumentos y devuelva su m谩ximo sin usar el m茅todo Math.max.

    ```js
    console.log(findMax(0, 10, 5));
    10;
    console.log(findMax(0, -10, -2));
    0;
    ```

### Ejercicios: Nivel 2

1. La ecuaci贸n lineal se calcula de la siguiente manera: _ax + by + c = 0_. Escribe una funci贸n que calcule el valor de una ecuaci贸n lineal, _solveLinEquation_.
1. La ecuaci贸n cuadr谩tica se calcula de la siguiente manera: _ax2 + bx + c = 0_. Escribe una funci贸n que calcule el valor o los valores de una ecuaci贸n cuadr谩tica, _solveQuadEquation_.

   ```js
   console.log(solveQuadratic()); // {0}
   console.log(solveQuadratic(1, 4, 4)); // {-2}
   console.log(solveQuadratic(1, -1, -2)); // {2, -1}
   console.log(solveQuadratic(1, 7, 12)); // {-3, -4}
   console.log(solveQuadratic(1, 0, -4)); //{2, -2}
   console.log(solveQuadratic(1, -1, 0)); //{1, 0}
   ```

1. Declare una funci贸n llamada _printArray_. Toma un array como par谩metro e imprime cada valor del array.
1. Declare una funci贸n llamada _showDateTime_ que muestre la hora en este formato: 01/08/2020 04:08 usando el objeto Date.

   ```sh
   showDateTime()
   08/01/2020 04:08
   ```

1. Declare una funci贸n llamada _swapValues_. Esta funci贸n intercambia el valor de x a y.

   ```js
   swapValues(3, 4); // x => 4, y=>3
   swapValues(4, 5); // x = 5, y = 4
   ```

1. Declare una funci贸n llamada _reverseArray_. Toma un array como par谩metro y retorna el array invertido (no use el m茅todo reverse()).

   ```js
   console.log(reverseArray([1, 2, 3, 4, 5]));
   //[5, 4, 3, 2, 1]
   console.log(reverseArray(["A", "B", "C"]));
   //['C', 'B', 'A']
   ```

1. Declare una funci贸n llamada _capitalizeArray_. Toma un array como par谩metro y retorna el array - capitalizedarray.
1. Declare una funci贸n llamada _addItem_. Toma un elemento de pa艜ametro y retorna un array despu茅s de agregar el un elemento.
1. Declare una funci贸n llamada _removeItem_. Toma como par谩metro un index y retorna un array despu茅s de eleminar el elemento con ese index.
1. Declare una funci贸n llamada _sumOfNumbers_. Toma un n煤mero como par谩metro y suma todos los n煤meros en ese rango.
1. Declare una funci贸n llamada _sumOfOdds_. Toma un par谩metro num茅rico y suma todos los n煤meros impares en ese rango.
1. Declare una funci贸n llamada _sumOfEven_. Toma un par谩metro num茅rico y suma todos los n煤meros pares en ese rango.
1. Declare una funci贸n llamada _evensAndOdds_ . Toma un entero positivo como par谩metro y cuenta el n煤mero de pares e impares.

   ```sh
   evensAndOdds(100);
   El n煤mero de impares son 50.
   El n煤mero de pares es 51.
   ```

1. Escriba una funci贸n que tome cualquier n煤mero de argumentos y retorne la suma de los argumentos

   ```js
   sum(1, 2, 3); // -> 6
   sum(1, 2, 3, 4); // -> 10
   ```

1. Escriba una funci贸n _randomUserIp_ que genere una ip de usuario aleatoria.
1. Escriba una funci贸n _randomMacAddress_ que genere una direcci贸n mac aleatoria.
1. Declare una funci贸n llamada _randomHexaNumberGenerator_. Cuando se llama a esta funci贸n, genera un n煤mero hexadecimal aleatorio. La funci贸n retorna el n煤mero hexadecimal.

   ```sh
   console.log(randomHexaNumberGenerator());
   '#ee33df'
   ```

1. Declare una funci贸n llamada _userIdGenerator_. Cuando se llama a esta funci贸n, genera un id de siete caracteres. La funci贸n devuelve el id.

   ```sh
   console.log(userIdGenerator());
   41XTDbE
   ```

### Ejercicios: Nivel 3

1. Modifique la funci贸n _userIdGenerator_. Declare una funci贸n de nombre _userIdGeneratedByUser_. No toma ning煤n par谩metro pero toma dos entradas usando prompt(). Una de las entradas es la cantidad de caracteres y la segunda entrada es la cantidad de ID que se supone que se generar谩n.

   ```sh
   userIdGeneratedByUser()
   'kcsy2
   SMFYb
   bWmeq
   ZXOYh
   2Rgxf
   '
   userIdGeneratedByUser()
   '1GCSgPLMaBAVQZ26
   YD7eFwNQKNs7qXaT
   ycArC5yrRupyG00S
   UbGxOFI7UXSWAyKN
   dIV0SSUTgAdKwStr
   '
   ```

1. Escriba una funci贸n llamada _rgbColorGenerator_ que genera colores rgb

   ```sh
   rgbColorGenerator()
   rgb(125,244,255)
   ```

1. Escriba una funci贸n **_arrayOfHexaColors_** que retorna cualquier cantidad de colores hexadecimales en un array.
1. Escriba una funci贸n **_arrayOfRgbColors_** que retorna cualquier cantidad de colores RGB en un array.
1. Escriba una funci贸n **_convertHexaToRgb_** que convierta el color hexa a rgb y retorna un color rgb.
1. Escriba una funci贸n **_convertRgbToHexa_** que convierta rgb a color hexa y retorna un color hexa.
1. Escriba una funci贸n **_generateColors_** que pueda generar cualquier n煤mero de colores hexa o rgb.

   ```js
   console.log(generateColors("hexa", 3)); // ['#a3e12f', '#03ed55', '#eb3d2b']
   console.log(generateColors("hexa", 1)); // '#b334ef'
   console.log(generateColors("rgb", 3)); // ['rgb(5, 55, 175)', 'rgb(50, 105, 100)', 'rgb(15, 26, 80)']
   console.log(generateColors("rgb", 1)); // 'rgb(33,79, 176)'
   ```

1. Llame a su funci贸n _shuffleArray_, toma un array como par谩metro y devuelve un array mezclada
1. Llame a su funci贸n _factorial_, toma un n煤mero entero como par谩metro y devuelve un factorial del n煤mero.
1. Llame a su funci贸n _isEmpty_, toma un par谩metro y verifica si est谩 vac铆o o no.
1. Llame a su funci贸n _sum_, toma cualquier cantidad de argumentos y devuelve la suma.
1. Escriba una funci贸n llamada _sumOfArrayItems_, toma un array como par谩metro y retorna la suma de todos los elementos. Compruebe si todos los elementos de la matriz son tipos de n煤meros. Si no, d茅 una respuesta razonable.
1. Escribe una funci贸n llamada _average_, toma un array como par谩metro y retorna el promedio de los elementos. Compruebe si todos los elementos de la matriz son tipos de n煤meros. Si no, d茅 una respuesta adecuada.
1. Escriba una funci贸n llamada _modifyArray_ que tome un array como par谩metro y modifique el quinto elemento del array y retorna el array. Si la longitud del array es inferior a cinco, retorna 'elemento no encontrado'.

   ```js
   console.log(modifyArray(['Avocado', 'Tomato', 'Potato','Mango', 'Lemon','Carrot']);
   ```

   ```sh
   ['Avocado', 'Tomato', 'Potato','Mango', 'LEMON', 'Carrot']
   ```

   ```js
   console.log(modifyArray(['Google', 'Facebook','Apple', 'Amazon','Microsoft',  'IBM']);
   ```

   ```sh
   ['Google', 'Facebook','Apple', 'Amazon','MICROSOFT',  'IBM']
   ```

   ```js
   console.log(modifyArray(['Google', 'Facebook','Apple', 'Amazon']);
   ```

   ```sh
     'Not Found'
   ```

1. Escribe una funci贸n llamada _isPrime_, que verifica si un n煤mero es un n煤mero primo.
1. Escriba una funci贸n que verifique si todos los elementos son 煤nicos en un array.
1. Escriba una funci贸n que verifique si todos los elementos de un array son del mismo tipo de datos.
1. El nombre de las variables de JavaScript no admite caracteres o s铆mbolos especiales, excepto \$ o \_. Escriba una funci贸n **isValidVariable** que verifique si una variable es v谩lida o inv谩lida.
1. Escriba una funci贸n que devuelva un array de siete n煤meros aleatorios en un rango de 0-9. Todos los n煤meros deben ser 煤nicos.

   ```js
   sevenRandomNumbers()[(1, 4, 5, 7, 9, 8, 0)];
   ```

1. Escriba una funci贸n llamada reverseCountries, toma el array de pa铆ses y primero copia el array y retorna el array original invertido
   馃帀 隆FELICITACIONES! 馃帀

[<< D铆a 6](../dia_06_Bucles/dia_06_bucles.md) | [D铆a 8 >>](../dia_08_Objetos/dia_08_objetos.md)
