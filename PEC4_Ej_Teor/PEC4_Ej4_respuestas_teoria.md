### Exercici 4 - Directives d'atribut i directives estructurals

<ins>**1.**</ins> - Explica què són i quan s'haurien d'utilitzar les variables locals següents de la directiva estructural *NgFor*:

• <ins>**index**</ins> - Representa l'índex actual del element en la iteració del bucle *NgFor*, és a dir, s'empra per accedir al element actual.<br>
```html
<div *ngFor="let item of items; let i = index">
  {{i + 1}}: {{item}}
</div>
```
• <ins>**even**</ins> - Retorna *true* si l'índex actual es parell, si no retornarà fals.<br>
• <ins>**odd**</ins> - Retorna *true* si l'índex actual es imparell, si no retornarà fals.<br>
```html
<div *ngFor="let item of items; let even = even; let odd = odd">
  <p *ngIf="even">Even: {{item}}</p>
  <p *ngIf="odd">Odd: {{item}}</p>
</div>
```
• <ins>**first**</ins> - Retorna *true* si l'element actual es el primer, sinó retornarà *false*.<br>
• <ins>**last**</ins> - Retorna *true* si l'element actual es el darrer, sinó retornarà *false*.<br>
```html
<div *ngFor="let item of items; let first = first; let last = last">
  <p *ngIf="first">First: {{item}}</p>
  <p *ngIf="last">Last: {{item}}</p>
</div>
```

<ins>**2.**</ins> -  Per què serveix l’opció TrackBy de la directiva estructural NgFor? Poseu exemples d'ús.<br>
- L'opció <ins>**TrackBy**</ins> s'utilitza per millorar el rendiment de **NgFor** al permetre fer un seguiment eficient dels canvis en la llista, doncs permet identificar quins elements han canviat, en lloc de tenir que renderitzar tota la llista.

```typescript
//Generador de claus úniques depenen de les propietats de l'element
trackByFn(index, item) {
  return generateKey(item);
}

generateKey(item) {
  return `${item.id}-${item.name}`;
}
```

<ins>**3.**</ins> -  És possible executar dues directives estructurals simultàniament? Explica la raó tant si és possible com si no ho és.<br>
- <ins>No, no és possible executar dues directives estructurals simultàniament</ins>, ja que aquestes directives manipulen el DOM, creant una complexitat i ambigüitat si s'executen al mateix temps.
- El que si seria possible seria adjuntar elements o contenidors, per tal de que tinguin un context diferent i evitar així certs conflictes.