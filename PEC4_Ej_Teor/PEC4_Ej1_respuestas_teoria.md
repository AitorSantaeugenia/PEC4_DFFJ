### Exercici 1 - Instal·lació i configuració d'Angular CLI

• <ins>ng new</ins> - Crea <ins>un nou projecte d'Angular</ins>. En l'exemple de la documentació d'[Angular](https://angular.io/cli ), podem veure que crea un projecte anomenat **my-first-project**:  <br>

```angular
ng new my-first-project
```

• <ins>ng generate</ins> - Aquesta opció s'utilitza per crear diferents opcions; components, directives, interfaces, serveis, etc. A continuació ho veurem amb més detall:<br>
- <ins>component</ins> - Crea un nou component genèric. Aquests son com a blocs que s'utilitzen per organitzar i encapsular la lògica i presentació de la interfície d'usuari. Sol generar arxius com un *Typescript*, un *HTML* i un *CSS*, així com un *arxiu de prova*.

```angular
ng generate component nom-component
```
- <ins>directive</ins> - Crea una nova directiva genèrica. Aquestes serveixen per modificar el comportament del *DOM*. Tal com amb la comanda anterior, també crea arxius adicionals (excepte el *HTML*).

```angular
ng generate directive nom-directiva
```
- <ins>enum</ins> - Crea un nou enumerat genèric per el projecte. Un enumerat son com un conjunt de constants amb certs noms significatius. També crea un arxiu adicional *Typescript*.
```angular
ng generate enum nom-enum
```
- <ins>guard</ins> - Serveix per crear una nova ruta "*guard*" genèrica, s'utilitza per evitar l'accés en determinades parts d'usuaris no autoritzats, per exemple. També crea un arxiu *Typescript*. 
```angular
ng generate guard nom-guard
```
- <ins>interface</ins> - Crea una nova interface genèrica. S'utilitza per crear un contracte de com ha de ser cert objecte. Crea un *Typescript* adicional.
```angular
ng generate interface nom-interface
```
- <ins>pipe</ins> - Crea una nova *pipe* genèrica. S'utilitzen per transformar dades en la interfície d'usuari. També crea un arxiu *Typescript* i un arxiu de prova. <br>
```angular
ng generate pipe nom-pipe
```
- <ins>service</ins> - Crea un nou servei en el projecte. Aquests son objectes que serveixen per encapsular la lògica i proporcionar certa funcionalitat. També genera un arxiu *Typescript* y un arxiu de prova.
```angular
ng generate service nom-servei
```

<code> Cal dir que aquestes comandes es poden escurçar possant:<br>
ng g c nom-component - Crea el component.<br>
ng g d nom-directiva - Crea la directiva.<br>
ng g e nom-enumerador - Crea el enumerador.<br>
ng g g nom-guard - Crea el guard.<br>
ng g i nom-interface - Crea la interface.<br>
ng g p nom-pipe - Crea el pipe.<br>
ng g s nom-servei - Crea el servei.<br>
</code>

• <ins>ng serve</ins> - S'utilitza per compilar l'aplicació i executar un servidor en entorn de desenvolupament. És recarregarà automàticament al crear canvis, com un *live server* de **Visual Studio Code* o altres. <br>
• <ins>ng test</ins> - Permet executar un entorn de proves unitàries mitjançant *Karma*, que es l'entorn de prova per a *Javascript*.<br>
• <ins>ng version</ins> - Mostra la versió actual d'Angular CLI i les dependències del teu projecte.<br>
