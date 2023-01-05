## **1.- Variables y operaciones**
#
**1.1 ¿Qué es una variable y para qué sirve?**
Una variable es una representación de un espacio en memoria, nos sirve para guardar datos.
#
**1.2 ¿Cuál es la diferencia entre declarar e inicializar una variable?**
Declarar una variable solo reserva espacio en memoria, sin un valor asignado, inicializar una variable es asignar un valor inicial a una variable.
#
**1.3 ¿Cuál es la diferencia entre sumar números y concatenar strings?**
Sumar numeros involucra una operación matemática, concatenar strings solo une cadenas una a lado de otra, por ejemplo, si tenemos "1" + "1" el resultado será "11" y no 2.
#
**1.4 ¿Cuál operador me permite sumar o concatenar?**
El operador +.
#
**Determinar el nombre y tipo de dato para almacenar en variables la siguiente información:**
#
**Nombre**
var name
tipo String
#
**Apellido**
var lastName
tipo String
#
**Nombre de usuario en Platzi**
var username
tipo String
#
**Edad**
var age
tipo Number
#
**Correo electrónico**
var email
tipo String
#
**Mayor de edad**
var isAdult
tipo Boolean
#
Dinero ahorrado
var savings
tipo Number
#
**Deudas**
var debts
tipo Number
#
**Traduce a codigo Javascript**


```
var name = 'John';
var lastname = 'Doe';
var username = 'johnd'
var age = 20;
var email = 'email@example.com'
var isAdult = true;
var savings = 15000;
var debts = 4000;
```
Calcula e imprime:
Nombre completo
```
var fullname = name + ' ' + lastname;
console.log(fullname);
```
Dinero real
```
var realMoney = savings - debts;
console.log(realMoney);
```

## **2.- Funciones**
#
**2.1 ¿Qué es una función?**
Es una secuencia de instrucciones que nos permiten realizar tareas
#
**2.2 ¿Cuándo me sirve usar una función en mi código?**
Es útil cuando queremos definir tareas que vayamos a repetir en nuestro código.
#
**2.3 ¿Cuál es la diferencia entre parámetros y argumentos de una función?**
Los parámetros son los que defines al momento de declarar una funcion, los argumentos son los que le pasas a una funcion cuando la estas utilizando.
#
**Convertir a una función**
```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

function greet(completeName, nickname){
console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
}

greet(completeName, nickname);
```
#
## **3.- Condicionales**
#
**3.1 ¿Qué es un condicional?**
Una condicional es una estructura de codigo que nos permite tomar decisiones en base a si condición es verdadera o falsa.
#
**3.2 ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?**
Las condicionales de javascript son el if-else y switch, la principal diferencia es que el switch nos permite analizar varias condiciones sin necesidad de incluir muchos if-else, que volverían nuestro código menos legible.
#
**3.3 ¿Puedo combinar funciones y condicionales?**
Si
#
**Replica el comportamiento del codigo de switch a if-else**
```
const tipoDeSuscripcion = "Basic";

if(tipoDeSuscripcion === "Free") {
       console.log("Solo puedes tomar los cursos gratis";
} else if (tipoDeSuscripcion === "Basic"){
	console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if (tipoDeSuscripcion === "Expert"){
   	console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else if (tipoDeSuscripcion === "ExpertPlus"){
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
```
#
**Replicar ahora solo con if**
```
const tipoDeSuscripcion = "Basic";

function checkSubscription(tipoDeSuscripcion){

	if(tipoDeSuscripcion === "Free") {
       		console.log("Solo puedes tomar los cursos gratis";
		return;
	}
	if (tipoDeSuscripcion === "Basic"){
		console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
		return;
	}
	if (tipoDeSuscripcion === "Expert"){
   		console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
		return;
	}
	if (tipoDeSuscripcion === "ExpertPlus"){
       		console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
		return;
	}
}

checkSubscription(tipoDeSuscripcion);
```
**Bonus: un solo condicional**
```
const tipoDeSuscripcion = "Basic";

function checkSubscription(tipoDeSuscripcion){	
		var subs= [
			{
			type: "Free",
			message: "Solo puedes tomar los cursos gratis"},
			{
			type: "Basic",
			message: "Puedes tomar casi todos los cursos de Platzi durante un mes"},
			{
			type: "Expert",
			message: "Puedes tomar casi todos los cursos de Platzi durante un año"},
			{
			type: "ExpertPlus",
			message: "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"}
		];

		var answer = subs.find(sub => {
			return sub.type === tipoDeSuscripcion;
		});
		
		console.log
		if(answer !== undefined){
			console.log(answer.message);
		} else {
			console.log('No se encontró el tipo de suscripción');
		}
}

checkSubscription(tipoDeSuscripcion);
```


## **4.- Ciclos**
#
**4.1 ¿Qué es un ciclo?**
Es una estructura que ejecuta instrucciones mientras que cierta condición se cumpla.
#
**4.2 ¿Qué tipos de ciclos existen en JavaScript?**
El tipo for y while, la diferencia entre ambas es que para el for conocemos la cantidad de veces que queremos que se ejecute nuestro codigo, para el while no.
#
**4.3 ¿Qué es un ciclo infinito y por qué es un problema?**
Un ciclo infinito es aquel cuya condicion se cumple todo el tiempo, esto es un problema por que un programa no podria avanzar mas alla del punto del ciclo, dependiendo del codigo, acaparara mas espacio en memoria y podria congelar el equipo donde se ejecuta.
#
**4.4 ¿Puedo mezclar ciclos y condicionales?**
Si.
#
**Replicar el comportamiento usando while**
```
var i = 0;
while(i <5){
	console.log("El valor de i es: " + i);
	i++;
}

i = 10;

while(i>=2){
	console.log("El valor de i es: " + i);
	i--;
}
```
**Escribir código para preguntar cuanto es 2+2**
```
answer = 0;
while(answer != 4){
	answer = prompt('Cuanto es 2 + 2?');
}
```
## **5.- Listas**
#
**5.1 ¿Qué es un array?**
Es un objeto que nos permite crear listas de datos de cualquier tipo y almacenarlas en una variable.
#
**5.2 ¿Qué es un objeto?**
Es un tipo de dato que puede tener propiedades asignadas, estas propiedades pueden ser de cualquier tipo, incluso otros objetos.
#
**5.3 ¿Cuándo es mejor usar objetos o arrays?**
Cuando queramos agrupar datos, se usan objetos cuando queremos asociar nombres a las propiedades, usamos arrays cuando queremos que sus 'nombres' sean números.
#
**5.4 ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?**
Si
#
**Crear una función que recibe un array e imprime el 1er elemento**
```
function printFirstElement(myList){
	console.log(myList[0]);
}
```
**Crear una función que recibe un array e imprime cada elemento**
```
function printArray(myList){
	for(item of myList){
		console.log(item);
	}
}
```
**Crear una funcion que recibe un objeto e imprime sus elementos**
```
function printObject(myObject){
	for(property in myObject){
		console.log(property +": "+ myObject[property]);
	}
}
```
