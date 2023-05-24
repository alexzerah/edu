# 2. GSAP Scroll trigger

## Installation

Vous pouvez installer :

- Via un CDN
- Sur le site de GreenSock
- Via import (recommandé)

```bash
npm i gsap
```

Dans votre fichier js :

```js
import { ScrollTrigger } from "gsap/ScrollTrigger.js";

// ...

gsap.registerPlugin(ScrollTrigger);

// ...
```

## Définition

ScrollTrigger permet de déclencher une action lorsqu’un élément apparait sur la page (au scroll).
Exemple : Vous voulez animer un carré jaune 🟨 lorsque vous l’atteignez (à 50% du viewport).

## Utilisation

[Lien codepen](https://codepen.io/alexzerah/pen/gOBqKxZ)

```html
<section class="s1"></section>
<section class="s2">
  <div class="el"></div>
</section>
<section class="s3"></section>

<style>
section {
  height: 100vh;
  position: relative;
}

.s1 {
    background-color: red;
}

.s2 {
  background-color: blue;
}

.s3 {
  background-color: green;
}

.el {
  background-color: yellow;
  height: 50px;
  width: 50px;
  top: 50%;
  position: absolute;
}
</style>
```

```js
gsap.registerPlugin(ScrollTrigger);

gsap.to(".el", {scrollTrigger: {
  trigger: ".el",
  start: "top +50%",
  end: "bottom",
  markers: true,
}, duration: 3, x: "95vw"})
```

## Paramètres

- `trigger` : Element qui sera utilisé comme déclencheur de l’animation. 
- `start` : Point où l’animation va commencer par rapport à la position du trigger.  Ici l’animation commence quand le top de l’élément se trouve à 50% de la hauteur du viewport.
- `end` : Point où l’animation va se terminer. Ici l’animation s’arrête lorsque le bottom de l’élément atteint le haut du viewport.
- `markers` :  Si `true`, outils de déboggage qui affiche les points de débuts et de fin de l’animation.


[1]:	https://codepen.io/alexzerah/pen/gOBqKxZ?editors=1111