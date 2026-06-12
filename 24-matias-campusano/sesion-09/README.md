#Sesion-09 05/05
### Interacciones con el teclado

*	Por Enter o mouse

*	Por teclas específicas (ej.
Números): Puedes hacer que la
tecla 1 te lleve al inicio, la 2 a la
experiencia y la 3 al final.

Ejemplo: 

function keyPressed() {
  if (key === ' ' || keyCode === ENTER) { // ' ' es el espacio
    estado = estado + 1;
    if (estado > 2) estado = 0;
  }
}

### Botones en la pantalla

Creación de botones con ayuda de la librería de P5.js en código HTML.

Ejemplo (esto requiere generar una variable y declararla en el Setup): 

let botonSiguiente;

function setup() {
  createCanvas(400, 400);
  textAlign(CENTER, CENTER);
  
  // Creamos el botón y le ponemos texto
  botonSiguiente = createButton('Siguiente Pantalla');
  botonSiguiente.position(150, 350); // Posición en la pantalla
  
  // Cuando se haga clic en ÉSTE botón, se ejecuta la función cambiarEstado
  botonSiguiente.mousePressed(cambiarEstado);
}

### Zonas de click

Si no quieres usar botones de
HTML y prefieres dibujar tus
propios botones con rect() o imágenes en Illustrator, png, etc.
puedes evaluar si el mouse
estaba dentro de esa caja al
hacer clic.

Ejemplo: 

function mousePressed() {
  // Imaginemos un botón dibujado en X: 100, Y: 50, Ancho: 200, Alto: 50
  if (mouseX > 100 && mouseX < 300 && mouseY > 50 && mouseY < 100) {
    estado = estado + 1;
    if (estado > 2) estado = 0;
  }
}
