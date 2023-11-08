-
## petit truc musical avec javascript
Lien de deploiement : https://ounissasadaoui.github.io/clavier_musical/

je n'ai pas pu trouver les vrais sons des "keys" d'une batterie, du coup j'ai pris plusieurs autres sons 

# première étape, le html/CSS 
il faut encore que j'arrange un peu mon display en css, il n'est pas super parfait

# deuxième  étape, le js
alors j'ai appris qu'au lieu de mettre en script le lien vers le js, on peut juste l'ecrire **directement** dans la balise script ** !
*la création d'un script à part est quand même une meilleure pratique, surtout pour des projects importants

j'ai appris à écrire des petites fonctions sur des eventlisteners, et à ajouter une classe css à un evenement javascript , comme ceci: qui ajpoute la classe css playing à key
```js
key.classList.add("playing");
```

## Comment ça marche?

pour chaque touche, on a cette partie dans une div:
```html
  <div class="keys">
    <div data-key = "65" class="key"><kbd>A</kbd> 
     <span class="sound">Win Drum</span>
    </div>
```
avec à chaque son, la touche sur laquelle il faut appuyer, son code (le data key)

et ensuite la span qui renvoit à la class du son
```html
  <audio data-key="65" src="./asset/mixkit-achievement-win-drums-555.wav"></audio>
```

Puis avec le script JavaScript, on crée la focntion qui appelle le bon son à chaque clé appuyée.
Et voilà !!

date: 17 mars 2023
