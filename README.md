# PAC4 - Desenvolupament front-end amb frameworks Javascript

## Dades del alumne

- asantaeugenia@uoc.edu
- Aitor Javier Santaeugenia Marí
- En aquesta PAC hem realitzat varis exercicis; <br>
    - <ins>**Exercici 1**</ins> - Instal·lació d'*Angular* i contestació d'algunes preguntes sobre certes opcions d'<ins>*Angular CLI*</ins>.<br><br>
    - <ins>**Exercici 2**</ins> - Un exercici amb algunes preguntes <ins>sobre certs arxius de configuració d'Angular</ins> al realitzar la comanda de creació, en el nostre cas: <code>ng new ecommerce</code>, una pregunta sobre <ins>*decoradors*</ins> i utilització te <ins>templateUrl/styleUrls</ins> en front a <ins>template/style</ins>.<br><br>
    - <ins>**Exercici 3**</ins> - En aquest exercici hem creat el primer component amb *Angular*, el component anomenat <ins>**article-item**</ins>, el qual s'ha de crear amb una **interfície** amb certs paràmetres i desprès aplicarem certes opcions com poden ser: un botó per incrementar/disminuir la quantitat que vol l'usuari i la visualització d'un color diferent al saber si el producte està o no en venda.<br>
    A continuació podem veure l'exercici com va quedar després d'aquest punt:<br>

    <div align="center">
    <img width="300px" src="https://i.imgur.com/LjuhZb5.png"/>
    </div><br>

    - Podem veure que <ins>em vaig avançar un poc</ins>, ja que en aquest punt vaig decidir mostrar dos articles (el mateix repetit, però amb diferents paràmetres), on un està en *stock* i l'altre no. Això <ins>ho vaig realitzar per poder veure la diferenciació de color</ins>.
    - Mostrem un missatge de *"Out of stock"* si no està a la venda.
    - Mostrem el preu en vermell i ratllat si no està en venda.
    - Cal dir que no vam mostrar el missatge de la quantitat d'unitat en *stock*, ja que a l'exercici demana la quantitat, i parla de quantitat amb el botó d'increment. Així que vam pensar que no feia falta la quantitat de *lestoc* (al mateix temps, a la imatge proporcionada no apareix).

    ```typescript
    //Això es com va quedar la interface amb les dades que ens demanen
    export interface ArticleItemComponentDataType{
        name:string,
        imageUrl:string,
        price:number,
        isOnSale:boolean,
        quantityInCart: number,
    }
    ```

    - <ins>**Exercici 4**</ins> - Exercici amb preguntes sobre les **directives**, tant d'atribut com estructurals. Sens demana informació sobre *NgFor* i certes variables d'aquesta així com del *TrackBy*.<br><br>
    - <ins>**Exercici 5**</ins> - En aquest exercici s'ens demana modificar el color del preu (<code>cal dir que nosaltres ho vam fer en el punt 3</code>) si no està disponible l'article. Al mateix temps, si no està disponible amagar els botons.

     <div align="center">
    <img width="300px" src="https://i.imgur.com/0iiHFDS.gif"/>
    <p>Podem veure que per molt que intentis comprar més de 10, si en stock n'hi ha 10, no et deixarà.
    </div>
    
    - Podem veure, en <ins>contrast amb l'exercici 3</ins> que ara el color apareix en gris en lloc d'en vermell com abans.
    - També que els botons desapareixen si no hi ha l'article a l'estoc.
    - Al mateix temps, hem aplicat la funcionalitat que <code>l'usuari no pugui "*comprar*" més quantitat de la que hi ha en stock</code>. Tot i que no ens ho demana l'anunciat, vam creure oportú fer-ho.<br><br>

    - <ins>**Exercici 5**</ins> - En aquest exercici hem de contestar a certes preguntes sobre la teoria dels components. Des de saber què és *style encapsulation*, saber que és el *shadow DOM*, el *changeDetection* o saber analitzar el cicle de vida d'un component dins d'*Angular*.