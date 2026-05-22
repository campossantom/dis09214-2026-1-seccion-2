# sesión 04 - 23/03
# DATOS DINÁMICOS Y VARIABLES — p5.js

## 1. Movimiento y Datos Dinámicos

En p5.js podemos crear movimiento usando variables dinámicas que cambian constantemente.

Ejemplo:

```javascript id="5wzxqv"
ellipse(mouseX, mouseY, 100, 100);
```

## 2. Variables Integradas en p5.js

### Mouse

#### `mouseX`

Posición horizontal del mouse.

```javascript id="3sfj6t"
ellipse(mouseX, 200, 50, 50);
```

#### `mouseY`

Posición vertical del mouse.

```javascript id="p6e0ow"
ellipse(200, mouseY, 50, 50);
```

#### `pmouseX`

Posición anterior del mouse.

#### `mouseIsPressed`

Detecta si el mouse está presionado.

```javascript id="quqk9n"
if (mouseIsPressed) {
  background(0);
}
```

#### `mouseButton`

Detecta qué botón del mouse se usa.

* LEFT
* RIGHT
* CENTER

### Lienzo

#### `width`

Ancho del canvas.

#### `height`

Alto del canvas.

```javascript id="ty0l0f"
ellipse(width/2, height/2, 100, 100);
```

### Ventana

#### `windowWidth`

Ancho total de la ventana.

#### `windowHeight`

Alto total de la ventana.

```javascript id="6ysxcm"
createCanvas(windowWidth, windowHeight);
```

### Teclado

#### `key`

Última tecla presionada.

```javascript id="ybjlwm"
text(key, 100, 100);
```

#### `keyCode`

Código de teclas especiales.

```javascript id="l1r7gi"
if (keyCode === ENTER) {
  background(255);
}
```

#### `keyIsPressed`

Detecta si una tecla está presionada.

### Tiempo

#### `frameCount`

Cantidad de frames desde el inicio.

#### `deltaTime`

Tiempo entre frames.

## 3. Crear Tus Propias Variables

### Variables dinámicas

```javascript id="xv8rj8"
let x;
```

### Variables constantes

```javascript id="49d8d6"
const tamaño = 100;
```

### Inicializar Variables

```javascript id="3vqg9p"
let x = 200;
```

### Usar Variables

```javascript id="c4x6nf"
ellipse(x, 100, 50, 50);
```

## 4. JavaScript Objects

Sirven para organizar varias variables dentro de una sola estructura.

### Ejemplo

```javascript id="p9o1wg"
let persona = {
  x: 100,
  y: 200,
  size: 50
};

ellipse(persona.x, persona.y, persona.size);
```

### Acceso a datos

```javascript id="0g6mjt"
persona.x
persona.y
```

## 5. `random()`

Genera números aleatorios.

### `random()`

Número entre 0 y 1.

```javascript id="txs2wy"
random();
```

### `random(maximo)`

Número entre 0 y el máximo.

```javascript id="8xkfrw"
random(100);
```

### `random(minimo, maximo)`

Número entre dos valores.

```javascript id="gx0gsd"
random(20, 50);
```

### Ejemplo

```javascript id="rf9xrp"
let x = random(width);
let y = random(height);

ellipse(x, y, 50, 50);
```

## 6. `map()`

Transforma un valor de un rango a otro.

### Sintaxis

```javascript id="ptx3va"
map(valor, min_original, max_original, min_nuevo, max_nuevo);
```

### Ejemplo

```javascript id="n5qep8"
let tamaño = map(mouseX, 0, width, 10, 200);

ellipse(200, 200, tamaño);
```

### Explicación

* `mouseX` → valor original
* `0 y width` → rango original
* `10 y 200` → nuevo rango

## 7. Width y Height

Variables del tamaño del canvas.

```javascript id="4n5n72"
createCanvas(800, 600);

ellipse(width/2, height/2, 100, 100);
```

## 8. WindowWidth y WindowHeight

Ajustan el canvas al tamaño de la ventana.

```javascript id="v4psg0"
createCanvas(windowWidth, windowHeight);
```

## 9. Ejemplo Completo

```javascript id="6w9fkp"
let x;

function setup() {
  createCanvas(windowWidth, windowHeight);
  x = width/2;
}

function draw() {
  background(220);

  let tamaño = map(mouseX, 0, width, 20, 200);

  fill(random(255), random(255), random(255));

  ellipse(x, mouseY, tamaño);

  x = x + 1;

  if (x > width) {
    x = 0;
  }
}
```

## 10. Checklist de la Clase

Debes usar:

* `mouseX`
* `mouseY`
* Variables propias (`let`)
* JavaScript Objects
* `random()`
* `width`
* `height`
* `windowWidth`
* `windowHeight`
* `map()`

## 11. Conceptos Importantes

| Concepto                     | Función               |
| ---------------------------- | --------------------- |
| Variables                    | Guardan datos         |
| Objects                      | Organizan información |
| `random()`                   | Genera azar           |
| `map()`                      | Cambia escalas        |
| `mouseX / mouseY`            | Detectan mouse        |
| `width / height`             | Tamaño canvas         |
| `windowWidth / windowHeight` | Tamaño ventana        |
