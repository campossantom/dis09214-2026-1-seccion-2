# sesión 05 
# DATOS DINÁMICOS Y VARIABLES EN p5.js

## Variables integradas

### Posición del mouse

```javascript
ellipse(mouseX, mouseY, 50, 50);
```

- `mouseX` → posición horizontal
- `mouseY` → posición vertical

---

## Variables del canvas

```javascript
width
height
```

Representan el tamaño del lienzo.

---

## Crear variables propias

```javascript
let x = 100;
let velocidad = 2;
```

`let` sirve para crear variables dinámicas.

---

## Movimiento básico

```javascript
let x = 0;

function setup() {
  createCanvas(500, 500);
}

function draw() {
  background(220);

  circle(x, 250, 50);

  x = x + 2;
}
```

---

## random()

Genera números aleatorios.

```javascript
random(100);
```

Número entre 0 y 100.

### Ejemplo

```javascript
let tamaño;

function setup() {
  createCanvas(500, 500);
}

function draw() {
  background(0);

  tamaño = random(20, 100);

  circle(mouseX, mouseY, tamaño);
}
```

---

## map()

Transforma valores de un rango a otro.

```javascript
map(valor, min1, max1, min2, max2);
```

### Ejemplo

```javascript
let tamaño;

function setup() {
  createCanvas(500, 500);
}

function draw() {
  background(220);

  tamaño = map(mouseX, 0, width, 20, 200);

  circle(250, 250, tamaño);
}
```

---

## windowWidth y windowHeight

Permiten que el canvas se adapte a la pantalla.

```javascript
createCanvas(windowWidth, windowHeight);
```

---

## Ejemplo completo

```javascript
let x = 0;
let tamaño;

function setup() {
  createCanvas(windowWidth, windowHeight);
}

function draw() {
  background(30);

  tamaño = map(mouseX, 0, width, 50, 200);

  fill(random(255), random(255), random(255));

  circle(x, height / 2, tamaño);

  x = x + 3;

  if (x > width) {
    x = 0;
  }
}
```

---

## Conceptos aprendidos

- Variables
- Movimiento
- mouseX y mouseY
- random()
- map()
- width y height
- windowWidth y windowHeight

---

## Links útiles

- https://p5js.org/es/
- https://p5js.org/reference/

