# sesión 06 - 14/04

loops y for

Definicion de bucle:  
Rizo de cabello en forma helicoidal  
Objeto cuya forma recuerda a un bucle  
Proceso que se repite indefinidiamente   
En Informatica, serie de instrucciones que se repiten indefinidamente mirnytsd no se cumpla una condicion previamente establecida   

LooP;  
Es una estructura de control que permite ejecutar un bloque de instrucciones de manera repetida, mientras se cumpla una condicion especifica hasta que se alcance un estado determinado  

While: Los bucles while son utiles para repetir instrucciones mientras una condicion sea verdadera. Son como sentencias if que se repite.  
While (condicion booleana) { si es true ejecute este codigo en bucle } 

Ejempplo  
Mientras (x sea menor o igual que el alto de mi lienzo) { x incrementara 1 cada vez }  
while (x <= height) { x=x+1 }   

for  
Una forma de repetir un bloque de código cuando se conoce el número  
de iteraciones. Los bucles `for` son útiles para repetir instrucciones un  
número determinado de veces.  
Son una especie de SHORTCUT para hacer loops y siempre tienen 4  
elementos:  

1. Inicialización de una variable  
2. Condición booleana (V-F)  
3. Actualización ( Incrementación o decrementación)  
4. Lo que queremos que pasé cuando la condición sea TRUE

 
For (inicializo variable;condicion booleana;actualizacion){    
lo que queremos que pase cuando la condicion sea verdadera}  

for(lex x=0 ; x <= widht; x=x+1) {  
ellipse(x,200,random(300))  }  



