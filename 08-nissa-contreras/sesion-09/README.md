# sesión 06 - 29/05

# Examén 

1. Perfeccionar la entrega de la solemne 2, o hacer una nueva, que representaba una problematica de genero  


## Carpeta de entrega
*

---

## ¿Qué es un diagrama de flujo? 

**Algoritmo:** Es una secuencia de instrucciones paso a paso, lógicas, definidas, ordenadas y finitas que permiten solucionar un problema o realizar una tarea específica.  

El diagrma de flujo es una representación gráfica de un algoritmo o de los pasos de un proceso. En programación, se utiliza como una herramienta de planificación para visualizar la lógica de un programa antes de escribir una sola línea de código.

**Input (Entrada):**  
La información o los ingredientes que necesitas para empezar.

**Proceso:** Los pasos lógicos que transforman esa entrada.

**Output (Salida):** El resultado final o la solución al problema.

---

## Array (listas) 

* Es como un contenedor con  compartimientos numerados donde puedes guardar múltiples datos bajo un mismo nombre. Es una lista que mantiene varios datos ordenados. Los arreglos (Arrays) son muy útiles para almacenar datos relacionados y pueden contener datos de cualquier tipo.

**Ejemplo**
* Imagina un tren con vagones (un tren de programación, por así decirlo): el tren en sí es el array, pero cada vagón es un elemento, y cada elemento puede contener lo que quieras: números enteros, variables, ¡incluso otros arrays!

**SINTAXIS**
let nombreArray =[e0, e1, e2, e3, e4, e5];  
let Colores = ["red", "orange", "yellow", "green", "blue"];

¿Cómo uso los elementos de este Array?  
* Para llamar a alguno de los valores de mi array vamos a usar: nombreArray [n° elemento]

* Ejemplo:
background (Colores[1]);
* Esto pintara el fondo de mi lienzo de color anaranjado.

* Ejemplo en p5
```
let Colores = ["red", "orange", "yellow", "green", "blue", "purple"];
let index = 0

function setup() {
  createCanvas(400, 400);
  frameRate(1);
}

function draw() {
  //background(Colores[2]);
  
  background(Colores[index]); 
  index = index + 1;
  print(index);
  
  if (index >= Colores.length) {
  index = 0;
 }
}
```

Elementos en p5:  
index: Recorre la lista que esta contenida en el Array de forma seguida, en la velocidad que uno le asigne.  
print: Imprime en la consola los datos que queremos visualizar.
length: Sirve para recetear los elementos del Array, para que funcione como bucle y estos se vayan repitiendo. Equivale al numero total de elementos que tiene mi Array.

---

## Class (molde)

* Una clase (class) es un molde o plantilla abstracta que define la estructura, los datos (propiedades) y los comportamientos (métodos) que tendrá un tipo de objeto específico.

**Ejemplo**  
* Imagínala como el plano de diseño de una casa o un molde para hacer galletas: no es el objeto real en sí, sino las instrucciones empaquetadas para fabricar infinitas copias independientes basadas en ese mismo modelo utilizando la palabra clave new

**SINTAXIS**
*  La sintaxis básica de una clase en JavaScript se estructura siempre en tres partes dentro de un bloque de llaves:  
1. La palabra clave class + nombre que le quiera dar.  
2. El método constructor (donde se definen las propiedades del objeto usando .this)  
3. Las funciones personalizadas que definen lo que hace el objeto.

Se escribe afuera y abajo del función draw(); :  
```
class cuadrado {
  constructor() {
    this.x = 150;
    this.y = 150;
  }

  move() {
    this.x = this.x + random(-5, 5);
    this.y = this.y + random(-5, 5);
  }
  show() {
    stroke(179, 255, 127);
    strokeWeight(4);
    noFill();
    rect(this.x, this.y, 200, 200);
  }
}
```

Y luego se crea en el setup(); :   
```
function setup() {
  createCanvas(500, 500);
  cuadrado1 = new cuadrado();
  cuadrado2 = new cuadrado();
  cuadrado3 = new cuadrado();
```

Y se llama a sus métodos en el draw();    
```
function draw() {
  background(129, 167, 242);

  cuadrado1.move();
  cuadrado1.show();
  cuadrado2.move();
  cuadrado2.show();
  cuadrado3.move();
  cuadrado3.show();
}
```

