## Soluciones a los Ejercicios de Transformaciones y Animaciones en CSS

### Ejercicio 1: Translate en el Eje X

```css
.element {
    transform: translateX(50px);
}
```

### Ejercicio 2: Translate en el Eje Y

```css
.element {
    transform: translateY(100px);
}
```

### Ejercicio 3: Rotate

```css
.element {
    transform: rotate(45deg);
}
```

### Ejercicio 4: Scale

```css
.element {
    transform: scale(1.5);
}
```

### Ejercicio 5: Skew en el Eje X

```css
.element {
    transform: skewX(20deg);
}
```

### Ejercicio 6: Skew en el Eje Y

```css
.element {
    transform: skewY(30deg);
}
```

### Ejercicio 7: Transformaciones Combinadas

```css
.element {
    transform: translate(50px, 100px) rotate(45deg) scale(1.5);
}
```

### Ejercicio 8: Transform Origin

```css
.element {
    transform-origin: top left;
    transform: rotate(45deg);
}
```

### Ejercicio 9: Perspective

```css
.container {
    perspective: 800px;
}

.element {
    transform: rotateY(45deg);
}
```

### Ejercicio 10: Rotate 3D

```css
.element {
    transform: rotate3d(1, 1, 0, 45deg);
}
```

## Animaciones Básicas

### Ejercicio 11: Transición de Color

```css
.element {
    transition: background-color 0.5s ease-in-out;
}

.element:hover {
    background-color: blue;
}
```

### Ejercicio 12: Transición de Tamaño

```css
.element {
    transition: transform 0.5s ease-in-out;
}

.element:hover {
    transform: scale(1.5);
}
```

### Ejercicio 13: Transición de Posición

```css
.element {
    transition: transform 0.5s ease-in-out;
}

.element:hover {
    transform: translateX(50px);
}
```

### Ejercicio 14: Transición de Opacidad

```css
.element {
    transition: opacity 0.5s ease-in-out;
}

.element:hover {
    opacity: 0.5;
}
```

### Ejercicio 15: Transición de Transformación

```css
.element {
    transition: transform 0.5s ease-in-out;
}

.element:hover {
    transform: translateX(50px) scale(1.5);
}
```

### Ejercicio 16: Transición de Bordes

```css
.element {
    transition: border-width 0.5s ease-in-out;
    border: 2px solid black;
}

.element:hover {
    border-width: 10px;
}
```

### Ejercicio 17: Transición de Sombras

```css
.element {
    transition: box-shadow 0.5s ease-in-out;
    box-shadow: 0 0 5px black;
}

.element:hover {
    box-shadow: 0 0 15px black;
}
```

### Ejercicio 18: Transición de Transformación de Esquinas Redondeadas

```css
.element {
    transition: border-radius 0.5s ease-in-out;
    border-radius: 0;
}

.element:hover {
    border-radius: 50%;
}
```

### Ejercicio 19: Transición de Gradiente

```css
.element {
    transition: background 0.5s ease-in-out;
    background: linear-gradient(to right, red, yellow);
}

.element:hover {
    background: linear-gradient(to right, blue, green);
}
```

### Ejercicio 20: Transición de Fuente

```css
.element {
    transition: font-size 0.5s ease-in-out;
}

.element:hover {
    font-size: 2em;
}
```

## Transformaciones Intermedias

### Ejercicio 21: Transformaciones 3D

```css
.container {
    perspective: 800px;
}

.cube {
    width: 100px;
    height: 100px;
    transform-style: preserve-3d;
    animation: rotateCube 5s infinite linear;
}

.cube div {
    position: absolute;
    width: 100px;
    height: 100px;
    background: rgba(255, 0, 0, 0.5);
}

.front  { transform: translateZ(50px); }
.back   { transform: rotateY(180deg) translateZ(50px); }
.left   { transform: rotateY(-90deg) translateZ(50px); }
.right  { transform: rotateY(90deg) translateZ(50px); }
.top    { transform: rotateX(90deg) translateZ(50px); }
.bottom { transform: rotateX(-90deg) translateZ(50px); }

@keyframes rotateCube {
    0% { transform: rotateX(0) rotateY(0); }
    100% { transform: rotateX(360deg) rotateY(360deg); }
}
```

### Ejercicio 22: Transición de Transformaciones Combinadas

```css
.element {
    transition: transform 0.5s ease-in-out;
}

.element:hover {
    transform: translateX(50px) rotate(45deg) scale(1.5);
}
```

### Ejercicio 23: Rotate 90 Grados

```css
.element {
    transform: rotate(-90deg);
}
```

### Ejercicio 24: Rotate con Origines Diferentes

```css
.element {
    transform-origin: bottom right;
    transform: rotate(45deg);
}
```

### Ejercicio 25: Scale para Hacer un Zoom

```css
.element {
    transform: scale(1.5);
}
```

### Ejercicio 26: Skew Combinado

```css
.element {
    transform: skewX(10deg) skewY(10deg);
}
```

### Ejercicio 27: Translate con Diferentes Unidades

```css
.element {
    transform: translate(10%, 2em);
}
```

### Ejercicio 28: Transformación Condicional

```css
.element.active {
    transform: rotate(45deg);
}
```

### Ejercicio 29: Rotate en el Eje Z

```css
.element {
    transform: rotateZ(45deg);
}
```

### Ejercicio 30: Múltiples Transformaciones en Secuencia

```css
.element {
    transform: translateX(50px);
    transform: rotate(45deg);
    transform: scale(1.5);
}
```

## Animaciones Intermedias

### Ejercicio 31: Animación de Desplazamiento

```css
@keyframes move {
    0% { transform: translateX(0); }
    100% { transform: translateX(100px); }
}

.element {
    animation: move 2s infinite alternate;
}
```

### Ejercicio 32: Animación de Rotación

```css
@keyframes rotate {
    0% { transform: rotate(0); }
    100% { transform: rotate(360deg); }
}

.element {
    animation: rotate 2s infinite linear;
}
```

### Ejercicio 33: Animación de Escalado

```css
@keyframes scale {
    0% { transform: scale(1); }
    100% { transform: scale(1.5); }
}

.element {
    animation: scale 2s infinite alternate;
}
```

### Ejercicio 34: Animación de Opacidad

```css
@keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
}

.element {
    animation: blink 1s infinite;
}
```

### Ejercicio 35: Animación de Fondo

```css
@keyframes changeColor {
    0% { background-color: red; }
    100% { background-color: blue; }
}

.element {
    animation: changeColor 2s infinite alternate;
}
```

### Ejercicio 36: Animación con Delay

```css
@keyframes move {
    0% { transform: translateX(0); }
    100% { transform: translateX(100px); }
}

.element {
    animation: move 2s infinite alternate 1s;
}
```

### Ejercicio 37: Animación Alternada

```css
@keyframes alternate {
    0% { transform: translateX(0); }
    100% { transform: translateX(100px); }
}

.element {
    animation: alternate 2s infinite alternate;
}
```

### Ejercicio 38: Animación con @keyframes Complejo

```css
@keyframes complex {
    0% { transform: translateX(0); }
    50% { transform: translateX(100px); }
    75% { transform: translateX(50px); }
    100% { transform: translateX(100px); }
}

.element {
    animation: complex 4s infinite;
}
```

### Ejercicio 39: Animación con Tiempo de Animación Variable

```css
@keyframes variable {
    0% { transform: translateX(0); }
    50% { transform: translateX(100px); }
    100

% { transform: translateX(50px); }
}

.element {
    animation: variable 4s infinite;
}
```

### Ejercicio 40: Animación de Texto

```css
@keyframes changeColor {
    0% { color: red; }
    100% { color: blue; }
}

.element {
    animation: changeColor 2s infinite alternate;
}
```

## Transformaciones Avanzadas

### Ejercicio 41: Transformaciones de Imagen

```css
.image {
    transform: rotate(45deg) scale(1.5);
}
```

### Ejercicio 42: Transformaciones Basadas en Eventos (HTML y CSS)

```css
.element:focus {
    transform: rotate(45deg);
}
```

### Ejercicio 43: Transformaciones en una Galería

```css
.gallery img {
    transition: transform 0.5s ease-in-out;
}

.gallery img:hover {
    transform: scale(1.1);
}
```

### Ejercicio 44: Transformaciones Responsivas

```css
.element {
    transform: scale(1);
}

@media (max-width: 600px) {
    .element {
        transform: scale(0.8);
    }
}
```

### Ejercicio 45: Transformaciones Anidadas

```css
.outer {
    transform: rotate(45deg);
}

.inner {
    transform: scale(1.5);
}
```

### Ejercicio 46: Transformaciones con Variables CSS

```css
:root {
    --rotation: 45deg;
}

.element {
    transform: rotate(var(--rotation));
}
```

### Ejercicio 47: Transformaciones con Pseudo-elementos

```css
.element::before {
    content: '';
    display: block;
    width: 100px;
    height: 100px;
    background: red;
    transform: rotate(45deg);
}
```

### Ejercicio 48: Transformaciones de Clip Path

```css
.element {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
    transform: rotate(45deg);
}
```

### Ejercicio 49: Transformaciones con Filtros

```css
.element {
    transform: scale(1.5);
    filter: blur(5px);
}
```

### Ejercicio 50: Transformaciones Basadas en Pseudoclases

```css
.element:hover {
    transform: rotate(45deg);
}
```

## Animaciones Avanzadas

### Ejercicio 51: Animaciones Basadas en Scroll (solo CSS)

```css
.element {
    position: sticky;
    top: 0;
    animation: scrollAnimation 1s forwards;
}

@keyframes scrollAnimation {
    from { transform: translateY(100px); opacity: 0; }
    to { transform: translateY(0); opacity: 1; }
}
```

### Ejercicio 52: Animaciones Sin Fisuras

```css
@keyframes seamless {
    0% { background-position: 0 0; }
    100% { background-position: 100% 0; }
}

.element {
    background: linear-gradient(90deg, red, yellow);
    background-size: 200% 100%;
    animation: seamless 10s infinite linear;
}
```

### Ejercicio 53: Animaciones con Interactividad (solo CSS)

```css
.element:hover {
    animation: hoverAnimation 1s forwards;
}

@keyframes hoverAnimation {
    from { transform: scale(1); }
    to { transform: scale(1.2); }
}
```

### Ejercicio 54: Animaciones en Secuencia

```css
@keyframes move {
    from { transform: translateX(0); }
    to { transform: translateX(100px); }
}

.element1 {
    animation: move 1s forwards;
}

.element2 {
    animation: move 1s forwards 1s;
}

.element3 {
    animation: move 1s forwards 2s;
}
```

### Ejercicio 55: Animaciones de Texto Avanzadas

```css
@keyframes typing {
    0% { width: 0; }
    100% { width: 100%; }
}

.element {
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid;
    width: 100%;
    animation: typing 3s steps(30) 1s infinite alternate;
}
```

### Ejercicio 56: Animaciones Responsivas

```css
@keyframes resize {
    from { transform: scale(1); }
    to { transform: scale(0.8); }
}

.element {
    animation: resize 2s infinite alternate;
}

@media (max-width: 600px) {
    .element {
        animation-duration: 4s;
    }
}
```

### Ejercicio 57: Animaciones en una Galería

```css
.gallery img {
    transition: transform 0.5s ease-in-out;
}

.gallery img:hover {
    animation: galleryHover 1s infinite;
}

@keyframes galleryHover {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}
```

### Ejercicio 58: Animaciones de Fondo Avanzadas

```css
@keyframes backgroundChange {
    0% { background-color: red; }
    50% { background-color: blue; }
    100% { background-color: green; }
}

.element {
    animation: backgroundChange 5s infinite;
}
```

### Ejercicio 59: Animaciones con Pseudo-elementos

```css
.element::before {
    content: '';
    display: block;
    width: 100px;
    height: 100px;
    background: red;
    animation: pseudoElementAnimation 2s infinite;
}

@keyframes pseudoElementAnimation {
    0% { transform: rotate(0); }
    100% { transform: rotate(360deg); }
}
```

### Ejercicio 60: Animaciones con @keyframes y Pseudoclases

```css
@keyframes hoverAnimation {
    from { transform: scale(1); }
    to { transform: scale(1.2); }
}

.element:hover {
    animation: hoverAnimation 1s forwards;
}
```

---

## [Autor: Alejandro Di Stefano](https://github.com/Drako01)
