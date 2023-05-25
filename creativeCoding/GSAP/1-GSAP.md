# 1. GSAP

## Qu’est-ce que GSAP ?

GSAP, ou GreenSock Animation Platform, est une bibliothèque JavaScript pour créer des animations

## Installation

### CDN

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.9.1/gsap.min.js"></script>
```

### Import JS

```bash
npm install gsap
```

```js
import { gsap } from "gsap";
```

(Vous devez être en type module)

### Tweens

Un "tween" est l'unité de base de l'animation avec GSAP. Un tween représente une transition entre deux états au fil du temps. Voici comment créer un tween

`gsap.to(".myElement", { duration: 1, x: 100 });`

Trois méthodes

- `gsap.to()` : Crée la transition entre l'état initial et l'état final.
- `gsap.from()` : Crée la transition depuis l'état initial vers l'état final.
- `gsap.fromTo()` : Crée la transition entre deux états définis.

```js
gsap.to('h1', {duration: 2, x: 100});
gsap.from('h1', {duration: 2, opacity: 0});
gsap.fromTo('h1', {duration: 2, opacity: 0}, {opacity: 100, x: 100});
```

### Timeline

Une timeline est un conteneur pour les tweens. Elle permet de contrôler plusieurs tweens en même temps.

```js
const tl = gsap.timeline();
tl.to('h1', {duration: 2, x: 100});
tl.from('h1', {duration: 2, opacity: 0});
tl.fromTo('h1', {duration: 2, opacity: 0}, {opacity: 100, x: 100});
```

### Easing

- easeIn : accélération au début
- easeOut : décélération à la fin
- easeInOut : accélération au début et décélération à la fin

L'animation par défaut est linéaire. Pour changer cela, il faut utiliser l'option `ease` dans les tweens.

```js
gsap.to('h1', {duration: 2, x: 100, ease: "bounce"});
```

- `Power0` (linear) : animation linéaire
- `Power1`
- `Power2`
- `Power3`
- `Power4`
- `Back`
- `Elastic`
- `Bounce`
- `Rough`
- `SlowMo`
- `Stepped`
- `Circ`
- `Expo`
- `Sine`
- `Custom`

### Décalage

Pour décaler le début d'une animation, il faut utiliser l'option `delay` dans les tweens.

```js
gsap.to('h1', {duration: 2, x: 100, delay: 2});
```

### Répétition

Pour répéter une animation, il faut utiliser l'option `repeat` dans les tweens.

```js
gsap.to('h1', {duration: 2, x: 100, repeat: 2});
```

#### Répétition infinie

Pour répéter une animation à l'infini, il faut utiliser l'option `repeat` dans les tweens.

```js
gsap.to('h1', {duration: 2, x: 100, repeat: -1});
```