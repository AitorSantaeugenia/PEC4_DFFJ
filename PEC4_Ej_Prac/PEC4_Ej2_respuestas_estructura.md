### Exercici 2 - Hola Món amb Angular

<ins>**1.**</ins> Quina ordre has d'utilitzar per crear un nou projecte Angular utilitzant Angular CLI anomenat ecommerce? (A les preguntes que us faci Angular CLI pots contestar utilitzant les opcions per defecte).<br>
Amb Angular Cli crea el projecte angular ecommerce i explica breument l'estructura i els fitxers que ha generat Angular CLI:<br>
- Fitxers de configuració a l'arrel del projecte:<br>
    - tsconfing.app.json
    - angular.json
    - package.json
    - .editorconfig,
    - .gitignore
    - …
- Directori node_modules
- Directori src:
    - index.html
    - main.ts
    - styles.css
    - Directori assets
    - Directori app
        - Fitxers app.component.*
        - Fitxers app.module.ts

<ins>**2.**</ins> Explica cadascun dels següents decoradors generats per Angular CLI, detallant cadascuna de les propietats que es defineixen a:
- app.module.ts - @NgModule (declarations, imports, providers, bootstrap).<br>
- app.component.ts - @Component (selector, templateUrl, styleUrls).<br><br>

<ins>**3.**</ins> És possible poder injectar el template i els estils en línia d'un component sense necessitat d'especificar-los a templateUrl, styleUrls? És recomanable fer-ho?<br>