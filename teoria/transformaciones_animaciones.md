# Transformaciones y Animaciones en CSS

## Índice

1. [Introducción](#introducción)
2. [Transformaciones en CSS](#transformaciones-en-css)
    - [translate()](#translate)
    - [rotate()](#rotate)
    - [scale()](#scale)
    - [skew()](#skew)
    - [Transformaciones combinadas](#transformaciones-combinadas)
    - [Transformaciones 3D](#transformaciones-3d)
        - [perspective()](#perspective)
        - [rotateX()](#rotatex)
        - [rotateY()](#rotatey)
        - [rotateZ()](#rotatez)
        - [translate3d()](#translate3d)
        - [scale3d()](#scale3d)
        - [skew3d()](#skew3d)
3. [Animaciones en CSS](#animaciones-en-css)
    - [Propiedad `transition`](#propiedad-transition)
    - [Propiedad `animation`](#propiedad-animation)
    - [Uso de `@keyframes`](#uso-de-keyframes)
    - [Propiedades de animación](#propiedades-de-animación)
    - [Animaciones múltiples](#animaciones-múltiples)
4. [Teoría de Pseudo-elementos](#teoría-de-pseudo-elementos)
5. [Conclusión](#conclusión)

## Introducción

CSS (Cascading Style Sheets) nos permite aplicar estilos a nuestras páginas web. Dos de las capacidades más poderosas de CSS son las transformaciones y las animaciones, que nos permiten manipular la apariencia de los elementos de manera dinámica y atractiva. En este tutorial, aprenderemos los conceptos básicos de transformaciones y animaciones en CSS, y cómo aplicarlos en nuestros proyectos.

## Transformaciones en CSS

Las transformaciones en CSS nos permiten cambiar la posición, tamaño, rotación e inclinación de los elementos. La propiedad `transform` es la clave para realizar estas transformaciones.

### translate()

La función `translate()` mueve un elemento desde su posición actual.

```css
.element {
    transform: translate(50px, 100px);
}
```

En este ejemplo, el elemento se mueve 50 píxeles a la derecha y 100 píxeles hacia abajo.

### rotate()

La función `rotate()` gira un elemento en el plano 2D.

```css
.element {
    transform: rotate(45deg);
}
```

Este ejemplo rota el elemento 45 grados en el sentido de las agujas del reloj.

### scale()

La función `scale()` cambia el tamaño de un elemento.

```css
.element {
    transform: scale(1.5, 2);
}
```

Este ejemplo aumenta el ancho del elemento en un 150% y la altura en un 200%.

### skew()

La función `skew()` inclina un elemento en un plano 2D.

```css
.element {
    transform: skew(30deg, 20deg);
}
```

Este ejemplo inclina el elemento 30 grados en el eje X y 20 grados en el eje Y.

### Transformaciones combinadas

Podemos combinar múltiples transformaciones en una sola propiedad `transform`.

```css
.element {
    transform: translate(50px, 100px) rotate(45deg) scale(1.5);
}
```

Este ejemplo mueve, rota y escala el elemento en una sola declaración.

### Transformaciones 3D

Además de las transformaciones 2D, CSS nos permite aplicar transformaciones en un espacio tridimensional. Esto agrega una dimensión adicional de profundidad a nuestras transformaciones.

#### perspective()

La propiedad `perspective()` establece la distancia entre el plano Z y el usuario para permitir las transformaciones 3D.

```css
.container {
    perspective: 800px;
}
```

La perspectiva se aplica a los elementos hijos de `.container`, lo que les permite transformarse en un espacio 3D.

#### rotateX()

La función `rotateX()` rota un elemento alrededor del eje X.

```css
.element {
    transform: rotateX(45deg);
}
```

Este ejemplo rota el elemento 45 grados alrededor del eje X.

#### rotateY()

La función `rotateY()` rota un elemento alrededor del eje Y.

```css
.element {
    transform: rotateY(45deg);
}
```

Este ejemplo rota el elemento 45 grados alrededor del eje Y.

#### rotateZ()

La función `rotateZ()` rota un elemento alrededor del eje Z (similar a `rotate()` en 2D).

```css
.element {
    transform: rotateZ(45deg);
}
```

Este ejemplo rota el elemento 45 grados alrededor del eje Z.

#### translate3d()

La función `translate3d()` mueve un elemento en el espacio 3D.

```css
.element {
    transform: translate3d(50px, 100px, 200px);
}
```

Este ejemplo mueve el elemento 50 píxeles a la derecha, 100 píxeles hacia abajo y 200 píxeles hacia adelante en el espacio 3D.

#### scale3d()

La función `scale3d()` cambia el tamaño de un elemento en el espacio 3D.

```css
.element {
    transform: scale3d(1.5, 2, 0.5);
}
```

Este ejemplo escala el elemento en un 150% en el eje X, un 200% en el eje Y y un 50% en el eje Z.

#### skew3d()

Aunque `skew3d()` no existe como una función específica en CSS, las transformaciones 3D pueden combinarse para crear efectos de inclinación tridimensional utilizando `rotate` y `skew` en conjunto.

```css
.element {
    transform: rotateX(30deg) skew(10deg, 5deg);
}
```

Este ejemplo aplica una rotación en el eje X combinada con una inclinación en el plano 2D.

## Animaciones en CSS

Las animaciones en CSS nos permiten cambiar gradualmente el estilo de un elemento desde un estado inicial a un estado final. Hay dos formas principales de aplicar animaciones: mediante la propiedad `transition` y mediante la propiedad `animation`.

### Propiedad `transition`

La propiedad `transition` permite que los cambios en las propiedades CSS ocurran de manera gradual.

```css
.element {
    transition: all 0.5s ease-in-out;
}

.element:hover {
    transform: scale(1.2);
    background-color: blue;
}
```

En este ejemplo, cuando el usuario pasa el mouse sobre el elemento, este se escala y cambia de color gradualmente en 0.5 segundos.

### Propiedad `animation`

La propiedad `animation` permite definir animaciones más complejas mediante el uso de `@keyframes`.

### Uso de `@keyframes`

La regla `@keyframes` define los estados intermedios de una animación.

```css
@keyframes example {
    0% {
        transform: translateX(0);
    }
    50% {
        transform: translateX(100px);
    }
    100% {
        transform: translateX(0);
    }
}

.element {
    animation: example 2s infinite;
}
```

En este ejemplo, el elemento se mueve 100 píxeles a la derecha y luego vuelve a su posición original en un bucle infinito.

### Propiedades de animación

Podemos controlar varios aspectos de una animación con propiedades adicionales.

```css
.element {
    animation-name: example;
    animation-duration: 2s;
    animation-timing-function: ease-in-out;
    animation-delay: 1s;
    animation-iteration-count: infinite;
    animation-direction: alternate;
    animation-fill-mode: forwards;
    animation-play-state: running;
}
```

- `animation-name`: Nombre de la animación definida en `@keyframes`.
- `animation-duration`: Duración de la animación.
- `animation-timing-function`: Función de temporización que define la velocidad de la animación.
- `animation-delay`: Retraso antes de que comience la animación.
- `animation-iteration-count`: Número de veces que se repite la animación.
- `animation-direction`: Dirección de la animación (normal, reverse, alternate, alternate-reverse).
- `animation-fill-mode`: Define cómo aplicar los estilos antes y después de la animación.
- `animation-play-state`: Estado de la animación (running, paused).

### Animaciones múltiples

Podemos aplicar múltiples animaciones a un elemento separándolas por comas.

```css
@keyframes move {
    0% {
        transform: translateX(0);
    }
    100% {
        transform: translateX(100px);
    }
}

@keyframes rotate {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
}

.element {
    animation: move 2s infinite, rotate 2s infinite;
}
```

En este ejemplo, el elemento se mueve y rota simultáneamente en un bucle infinito.

## Teoría de Pseudo-elementos

### ¿Qué son los Pseudo-elementos?

Los pseudo-elementos en CSS son palabras clave que se añaden a los selectores para seleccionar una parte específica de un elemento. Los pseudo-elementos permiten aplicar estilos a una parte concreta de un elemento sin necesidad de modificar el HTML. Los dos pseudo-elementos más comunes son `::before` y `::after`.

### Pseudo-elemento `::before`

El pseudo-elemento `::before` se utiliza para insertar contenido antes del contenido real de un elemento. Este contenido no existe en el HTML, pero se puede generar y estilizar usando CSS.

**Ejemplo:**

```css
/* Agrega un asterisco antes del contenido del párrafo */
p::before {
  content: "* ";
  color: red;
}
```

```html
<p>Este es un párrafo.</p>
```

**Resultado:**
*Este es un párrafo.

### Pseudo-elemento `::after`

El pseudo-elemento `::after` se utiliza para insertar contenido después del contenido real de un elemento. Al igual que `::before`, este contenido no existe en el HTML, pero se puede generar y estilizar usando CSS.

**Ejemplo:**

```css
/* Agrega un punto después del contenido del párrafo */
p::after {
  content: ".";
  color: blue;
}
```

```html
<p>Este es un párrafo</p>
```

**Resultado:**
Este es un párrafo.

### Usos Comunes de los Pseudo-elementos

1. **Decoraciones:** Añadir iconos, imágenes o decoraciones adicionales a elementos sin necesidad de cambiar el HTML.
2. **Citas:** Añadir comillas a elementos de bloque de citas.
3. **Limpieza de Flotantes:** Utilizar `::after` para limpiar elementos flotantes.
4. **Efectos de Estilo:** Crear efectos de estilo avanzados como bordes adicionales, sombras y más.

### Ejemplo Práctico

**CSS:**

```css
/* Añadir comillas a los elementos de bloque de citas */
blockquote::before {
  content: "“";
  font-size: 2em;
  color: gray;
}

blockquote::after {
  content: "”";
  font-size: 2em;
  color: gray;
}
```

**HTML:**

```html
<blockquote>La única forma de hacer un gran trabajo es amar lo que haces.</blockquote>
```

**Resultado:**

“ La única forma de hacer un gran trabajo es amar lo que haces. ”

## Conclusión

Las transformaciones y animaciones en CSS son herramientas poderosas que nos permiten crear interfaces web interactivas y dinámicas. Este tutorial cubre los conceptos básicos para comenzar a utilizar estas características en tus proyectos. Experimenta con diferentes combinaciones y propiedades para ver qué efectos puedes lograr.

## [Autor: Alejandro Di Stefano](https://github.com/Drako01)
