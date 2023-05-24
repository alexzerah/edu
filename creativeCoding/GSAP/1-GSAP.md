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
