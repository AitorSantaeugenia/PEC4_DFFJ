1. (0.75 punts) Quina ordre has d'utilitzar per crear un nou projecte Angular utilitzant
Angular CLI anomenat ecommerce? (A les preguntes que us faci Angular CLI pots
contestar utilitzant les opcions per defecte).
Amb Angular Cli crea el projecte angular ecommerce i explica breument
l'estructura i els fitxers que ha generat Angular CLI:
• Fitxers de configuració a l'arrel del projecte:
o tsconfing.app.json
o angular.json
o package.json
o .editorconfig,
o .gitignore
o …
• Directori node_modules
• Directori src:
o index.html
o main.ts
o styles.css
o Directori assets
o Directori app
▪ Fitxers app.component.*
▪ Fitxers app.module.ts

Desenvolupament front-end amb frameworks Javascript 22/11/2023 pàg. 7
2. (0.25 punts) Explica cadascun dels següents decoradors generats per Angular
CLI, detallant cadascuna de les propietats que es defineixen a:
• app.module.ts - @NgModule (declarations, imports,
providers, bootstrap).
• app.component.ts - @Component (selector, templateUrl,
styleUrls).
3. (0.25 punts) És possible poder injectar el template i els estils en línia d'un
component sense necessitat d'especificar-los a templateUrl, styleUrls? És
recomanable fer-ho?