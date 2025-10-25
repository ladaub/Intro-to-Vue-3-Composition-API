Note Vue
Lesson 2

1- Le fichier App.vue dans src est le top level des composant, c'est le composant dans lequel tout les autre fichiers composant seront liés
2- Quand nous regardons dans le ficher main.js, on peut s'appercevoir qu'il est le point d'entree de tout en utilisant la methode createApp a partir de 'vue'
3- L'application est montée via #app dans le fichier html
4- Dans le fichier App.vue, nous avons 2 partie: la partie du script et le template, de facon optionnelle, il y'a la section css
5- Le Template est le squelette qui donne au composant sa structure
6- La partie Script agit comme le cerveau ou est placé la logic et les fonctionnalites
7- import { ref } from 'vue'; cela est utilisé pour initialisé une partie de l'etat
8- ref est comme une boite qui stock une valeur; actuellement on a mis 'Socks' dans cette boite, Vue garde un oeil sur lui(ref), des que la valeur a l'interieur de ref change, tout ce qui est dans l'app et qui l'utlise se met a jour automatiquement
9- En utilisant un ref a l'interieur de notre template dans le H1, c'est comme si l'on a avait créer un lien direct de communication entre le template et le script, entre le HTML et Javascript