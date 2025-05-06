
# 🎨 Transiciones, Transformaciones y Animaciones en CSS

## 📚 Objetivos de esta unidad

- Comprender qué son las transiciones y cómo se usan en CSS.
- Usar transformaciones para cambiar la forma, tamaño y posición de un elemento.
- Crear animaciones simples con `@keyframes` y `animation`.
- Personalizar la duración, retraso, dirección y otras propiedades.

---

## 🧠 1. ¿Qué son las Transiciones?

Las **transiciones** permiten que los cambios en las propiedades CSS ocurran de forma suave en lugar de ser instantáneos.

### 📌 Ejemplo básico

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    .caja {
      width: 100px;
      height: 100px;
      background-color: red;
      transition: background-color 0.5s ease;
    }

    .caja:hover {
      background-color: blue;
    }
  </style>
</head>
<body>
  <div class="caja"></div>
</body>
</html>
````

### 🔍 Explicación

- `transition: background-color 0.5s ease;` → cambia el color en 0.5 segundos con una curva de animación suave.
- Cuando pasás el mouse por encima (`:hover`), el color cambia **suavemente** de rojo a azul.

---

## 🌀 2. Transformaciones

Las **transformaciones** permiten rotar, escalar, mover o inclinar un elemento.

### ✨ Tipos comunes de transformaciones

| Transformación    | Qué hace            |
| ----------------- | ------------------- |
| `translate(x, y)` | Mueve el elemento   |
| `scale(x)`        | Agranda o achica    |
| `rotate(deg)`     | Rota el elemento    |
| `skew(x, y)`      | Inclina el elemento |

### 📌 Ejemplo

```html
<style>
  .caja {
    width: 100px;
    height: 100px;
    background-color: green;
    transition: transform 0.5s;
  }

  .caja:hover {
    transform: rotate(45deg) scale(1.2) translate(20px, 10px);
  }
</style>

<div class="caja"></div>
```

---

## 🎬 3. Animaciones con Keyframes

Las **animaciones** permiten definir una serie de pasos para cambiar estilos con el tiempo.

### 🧩 ¿Qué es `@keyframes`?

Una regla que define **cómo cambian los estilos** en cada momento de la animación.

### 📌 Ejemplo

```html
<style>
  .pelota {
    width: 50px;
    height: 50px;
    background-color: orange;
    border-radius: 50%;
    animation: rebotar 2s infinite;
  }

  @keyframes rebotar {
    0%   { transform: translateY(0); }
    50%  { transform: translateY(-100px); }
    100% { transform: translateY(0); }
  }
</style>

<div class="pelota"></div>
```

### 🔍 Explicación

- `animation: rebotar 2s infinite;` → Usa la animación llamada `rebotar`, que dura 2 segundos y se repite siempre.
- El `@keyframes` indica los pasos de la animación (inicio, medio y fin).

---

## ⏱️ 4. Personalización de Animaciones y Transiciones

| Propiedad               | Qué hace                                                   |
| ----------------------- | ---------------------------------------------------------- |
| `duration` (`s` o `ms`) | Cuánto dura                                                |
| `delay`                 | Cuánto tarda en empezar                                    |
| `timing-function`       | Tipo de curva (por ej. `ease`, `linear`)                   |
| `direction`             | Sentido de la animación (`normal`, `reverse`, `alternate`) |
| `iteration-count`       | Cuántas veces se repite (`infinite` o un número)           |

### 📌 Ejemplo combinado

```html
<style>
  .cuadro {
    width: 100px;
    height: 100px;
    background-color: purple;
    animation: girar 3s ease-in-out 1s infinite alternate;
  }

  @keyframes girar {
    from { transform: rotate(0deg); }
    to   { transform: rotate(360deg); }
  }
</style>

<div class="cuadro"></div>
```

### 🔍 ¿Qué hace?

- Dura 3 segundos.
- Espera 1 segundo para empezar.
- Se repite para siempre (`infinite`).
- Va y vuelve (`alternate`).

---

## 🧪 5. Práctica guiada

### Ejercicio 1: Transición de color y tamaño

```html
<style>
  .boton {
    padding: 10px 20px;
    background-color: coral;
    color: white;
    border: none;
    transition: all 0.3s ease;
  }

  .boton:hover {
    background-color: darkred;
    transform: scale(1.1);
  }
</style>

<button class="boton">Pasa el mouse</button>
```

---

### Ejercicio 2: Animación de entrada

```html
<style>
  .mensaje {
    opacity: 0;
    animation: aparecer 2s forwards;
  }

  @keyframes aparecer {
    from { opacity: 0; transform: translateY(20px); }
    to   { opacity: 1; transform: translateY(0); }
  }
</style>

<div class="mensaje">Hola mundo animado</div>
```

---

## 📦 Recursos extra

- [Documentación oficial de MDN sobre CSS Transitions](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)
- [Transformaciones en CSS (MDN)](https://developer.mozilla.org/es/docs/Web/CSS/transform)
- [Animaciones en CSS (MDN)](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Animations)

---

## ✅ Resumen

| Tema                       | Qué hace                                   |
| -------------------------- | ------------------------------------------ |
| `transition`               | Cambia una propiedad suavemente            |
| `transform`                | Modifica forma/posición de un elemento     |
| `@keyframes` + `animation` | Define y ejecuta una animación paso a paso |

---

## 🧑‍🏫 Profesor  

👨‍💻 **Alejandro Daniel Di Stefano**  
📌 **Desarrollador Full Stack**  
🔗 **GitHub:** [Drako01](https://github.com/Drako01)  
