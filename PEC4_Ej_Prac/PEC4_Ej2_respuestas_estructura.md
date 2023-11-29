### Exercici 2 - Hola Món amb Angular

<ins>**1.**</ins> Quina ordre has d'utilitzar per crear un nou projecte Angular utilitzant Angular CLI anomenat ecommerce?.<br>

- L'ordre utilitzada per crear el projecte ecommerce ha estat:<br>
<code>ng new ecommerce</code><br>
![ng new ecommerce](https://i.imgur.com/conRUbs.png)<br>
![ng new ecommerce - done](https://i.imgur.com/gA0pfhj.png)
- Com podem veure, tenim <ins>**.git**</ins> ja inicialitzat per a la carpeta global de la <ins>**PEC4**</ins>, per això el que realitzarem nosaltres, es incloure el projecte d'*Angular* en el <ins>**.gitignore**</ins> i crear un nou <ins>**.git**</ins> amb només el projecte, ja que volem tenir tots dos a Github.<br>
- Cal dir però, que es millor inicialitzar d'aquesta manera per tal de tenir el app.module.ts inicialitzat:
<code>ng new ecommerce --no-standalone</code>

Podem veure els dos repos a:<br>
https://github.com/AitorSantaeugenia/PEC4_Ecommerce<br>
https://github.com/AitorSantaeugenia/PEC4_DFFJ

Amb Angular Cli crea el projecte angular ecommerce i explica breument l'estructura i els fitxers que ha generat Angular CLI:<br>
- Fitxers de configuració a l'arrel del projecte:<br>
    - <ins>tsconfing.app.json</ins> - Configuració de *Typescript* per al projecte. Defineix com es compilaran els arxius *Typescript* en funció al projecte.<br>
    - <ins>angular.json</ins> - Configuració principal d'*Angular* que conté informació sobre l'estructura del projecte, dependències, configuració de compilació, proves, entre altres.<br>
    - <ins>package.json</ins> - Arxiu de configuració dels paquets de *Node.Js* (*npm*) amb informació sobre les dependències del projecte, scripts, versions, etc.<br>
    - <ins>.editorconfig</ins> - Arxiu que defineix les regles d'estil per mantenir consistència en el codi font, com els estils de línia o la identació.
    - <ins>.gitignore</ins> - Especifica els arxius i carpetes que han de ser ignorats per *GIT*, com poden ser arxius o carpetes que han de ser ignorades per no ser versionats, arxius de configuració només en local, etc.<br>
    - <ins>tsconfig.spec.json</ins> - Arxiu de configuració per a proves unitàries (specs). Defineix la compilació i execució de les proves en *Typescript* ja que conté informació de la configuració del entorn d'execució de les proves i la inclusió d'arxius per a *Jasmine* (entorn de *testing*).
- Directori <ins>node_modules</ins> - Directori que conté les dependències del projecte. Creat al executar <code>npm install</code> al instal·lar les dependències del *package.json*.<br>
- Directori <ins>src</ins> - Directori principal on hi ha la majoría (si no tot) del codi font del projecte.<br>
    - <ins>index.html</ins> - Pàgina *HTML* principal cargada al iniciar l'aplicació al navegador.<br>
    - <ins>main.ts</ins> - Punt d'entrada principal per a l'aplicació d'*Angular*. Inicialitza el mòdul principal del projecte.<br>
    - <ins>styles.css</ins> - Arxiu dels estils globals de l'aplicació. <br>
    - Directori <ins>assets</ins> - Directori on es solen guardar arxius estàtics com imatges, fonts de lletres, etc.<br>
    - Directori <ins>app</ins> - Aquest directori conté els components, serveis, mòduls i altres arxius relacionats amb la lògica del projecte.<br>
        - Fitxers <ins>app.component.*</ins> - Arxius relacionats amb el component princiipal de l'aplicació. <br>
        - Fitxers <ins>app.module.ts</ins> - Arxiu que defineix el mòdul principal de l'aplicació, s'importen i configuren els components i serveis així com a altres mòduls necessaris pel projecte.<br>

<ins>**2.**</ins> Explica cadascun dels següents decoradors generats per Angular CLI, detallant cadascuna de les propietats que es defineixen a:
- <ins>app.module.ts - @NgModule (declarations, imports, providers, bootstrap)</ins>.<br>
<code>@NgModule - S'utilitza per configurar i definir el mòdul principal de l'aplicació d'*Angular*.</code>
    - <ins>declarations</ins>: *Array* de components, directives i *pipes* que pertanyen aquest mòdul. Son els elements que poden ser emprats en les plantilles d'aquest mòdul.<br>
    - <ins>imports</ins>: *Array* de mòduls amb els *exports* que s'han d'emprar en aquest mòdul, o els que s'han de poder accedir.<br>
    - <ins>providers</ins>: *Array* de proveedors de serveis disponibles per a la injecció de dependències en components i serveis d'aquest mòdul.<br>
    - <ins>bootstrap</ins>: Component principal que s'ha d'inicialitzar al arrancar l'aplicació. Component principal que va dins de <code>index.html</code><br>
- <ins>app.component.ts - @Component (selector, templateUrl, styleUrls)</ins>.<br>
<code>@Component - S'utilitza per definir les propietats d'un component.</code>
    - <ins>selector</ins>: Selector *CSS* que indica com s'identificarà aquest component en les plantilles *HTML*. 
    - <ins>templateUrl</ins>: *URL* de l'arxiu *HTML* que conté la plantilla del component.
    - <ins>styleUrls</ins>: *Array* de *URLs* d'arxius *CSS* que contenen els estils aplicats al component.

<ins>**3.**</ins> És possible poder injectar el template i els estils en línia d'un component sense necessitat d'especificar-los a templateUrl, styleUrls? És recomanable fer-ho?<br>
- Si es possible, ja que es poden emprar les plantilles i estils en línia. Això es pot realitzar emprant <ins>*template*</ins> i <ins>*styles*</ins> en lloc dels que diu l'anunciat (*templateUrl* i *styleUrls*). Podem veure un exemple a continuació:

```ts
@Component({
  selector: 'app-root',
  template: `
    <div>
      <h1>{{ title }}</h1>
      <p>Exemple d'estils en línia.</p>
    </div>
  `,
  styles: [`
    div {
      background-color: aqua;
      padding: 10px;
    }

    h1 {
      color: red;
    }
  `]
})
```

- Al cercar diferents fonts sobre les millors pràctiques, no he llegit cap que digui que no s'ha de fer o que es millor un o l'altre. Si que es veritat que en el temari de l'assignatura, el llibre de <ins>**Angular: Up and Running**</ins>, de *Shyam Seshadri*, de l'editorial <ins>O'REILLY</ins> [diu el següent](https://learning.oreilly.com/library/view/angular-up-and/9781491999820/ch04.html#idm139828135304192) al parlar del <ins>*templateUrl*</ins>.<br>
<code>*There is no impact on the final generated application as Angular compiles the code into a single bundle. The only reason you might want to split your template code into a separate file is to get nicer IDE features such as syntax completion and the like, which are specific to file extensions. Generally, you might want to keep your templates separate if they are over three or four lines or have any complexity.*</code><br>
- Al parlar de <ins>*stylesUrl*</ins>, el llibre de <ins>**Angular: Up and Running**</ins> [diu que](https://learning.oreilly.com/library/view/angular-up-and/9781491999820/ch04.html#idm139828135303568):<br>
<code>*The decision between using styles and styleUrls is one of personal preference and has no impact on the final performance of the application*.</code>

- Al mateix temps, si mirem la [documentació d'Angular](https://angular.io/guide/styleguide#style-05-04), podem veure que diu que <ins>si son més de 3 línies, es millor separar-ho</ins>.
- <code>Així que resumint, es millor emprar el *templateUrl* i el *styleUrls* si son més de 3 línies de codi.</code>
- Altres fonts d'interés:<br>
https://stackoverflow.com/questions/34673979/differences-of-using-component-template-vs-templateurl<br>
https://stackoverflow.com/questions/37638131/template-vs-templateurl-and-styles-vs-styleurls-performance <br>



