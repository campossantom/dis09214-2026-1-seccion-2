# sesión 06 - 12/05

### Paso 1 
Crear canvas con dimensiones dinamicas: 
(windowWidth, windowHeight) // Estas variables leen constantemente el

### Paso 2 
Crear un evento "windowResized()" 

function windowResized(){
resizeCanvas(windowWidth,windowHeight);
}

### Paso 3  
Usar valores relativos

Usaremos fracciones y proporciones (uso de fracciones)
Ej: Centro del lienzo: (width/2,height/2)
Ej: A un cuarto de l apantalla en eje x: (width*25)

*  Aprovechar el uso de mousePrint para acompañarse quizás en la diagramación y ubicar cosas, de todas formas hay que usar un pensamiento lógico racional y ubicar las cosas considerando la readaptación.

###Paso 4 
Incluir factor de referencia 
referencia= min(width,heigth)

Se crea una referencia global y la asignamos para que calcule el mínimo.

let referencia;
functcion setup(){
createCanvas(wind...
referencia=min(width,heigth);
}

fc draw(){
backg(0);

### Paso 5
Usar TRANSLATE - PUSH Y POP 
En lugar de provocar situaciones matematicas complejas, uso de push y pop. 
Usamos Translate para mover el origen del mundo.

Para que no deforme hay que calcular el tamaño (ejemplo bandera 3:2) 
let canvasWidth=min(windowWidth, (windowHeight+3)/2); 

RECORDAR en el push and pop el Translate cambia el 0,0 desde donde parte particularmente ese comando.

Siempre usando push y pop. Para figuras dentro de un elemento.



