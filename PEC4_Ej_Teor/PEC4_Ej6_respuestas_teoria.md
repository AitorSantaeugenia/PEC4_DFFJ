### Exercici 6 - Teoria de components

<ins>**1.**</ins> Quins són els style encapsulation dels components? Poseu un exemple d'ús de cadascun.<br>
- <ins>*Emulated*</ins>: - Valor predeterminat, estils encapsulats d'Angular mitjançant la generació d'atributs de selector únics per a cada component.
```typescript
@Component({
  selector: 'app-test',
  template: '<p>Test d'encapsulació d'estils</p>',
  styles: ['p { color: red; }'],
  encapsulation: ViewEncapsulation.Emulated,
})
export class TestComponent {}
```
- <ins>*None*</ins>: - Estils no encapsulats i s'apliquen globalment.
```typescript
@Component({
  selector: 'app-test',
  template: '<p>Test sense encapsulació d'estils</p>',
  styles: ['p { color: green; }'],
  encapsulation: ViewEncapsulation.None,
})
export class TestComponent {}
```
- <ins>*ShadowDom*</ins>: - Empra el *Shadow DOM* natiu del navegador, tancant la vista del component dins d'un amfitrió i aplicant estils aïllats.
```typescript
@Component({
  selector: 'app-test',
  template: '<p>Test amb Shadow DOM</p>',
  styles: ['p { color: blue; }'],
  encapsulation: ViewEncapsulation.ShadowDom,
})
export class TestComponent {}
```

<ins>**2.**</ins> Què és el shadow DOM?
- És una API que permet encapsular la implementació de components webs, amagant certs detalls i comportaments interns, separant així els estils i el comportament de la pàgina, evitant conflictes i millorant el rendiment.


<ins>**3.**</ins> Què és el changeDetection?
- Mecanisme d'*Angular* que determina si els valors de les propietats dels components han realitzat un canvi i, en cas afirmatiu, actualitza la vista.  

<ins>**4.**</ins> Quines diferències hi ha entre les estratègies Default i OnPush? Quan has d'usar una i altra? Avantatges i inconvenients.<br>
- La principal diferència està en el fet que <ins>*Default* sempre verificarà la revisió dels canvis en els components</ins>, mentre que <ins>*OnPush*</ins>, <ins>només</ins> ho realitzarà <ins>quan se li indiqui</ins>.
- <ins>*Default* seria convenient emprar-lo</ins> quan l'aplicació tingui una mida no molt gran o <ins>quan no hi hagi molta complexitat</ins> en la lògica, mentre que <ins>*OnPush* s'ha d'aplicar quan es vulgui optimitzar grans aplicacions, minimitzant els canvis</ins>.
- <ins>*Default* és més fàcil d'utilitzar</ins>, però <ins>pot afectar el rendiment</ins> en realitzar més comprovacions dels canvis de les que realment volem, mentre que <ins>*OnPush* permet millorar el rendiment</ins> en reduir les comprovacions dels canvis, però <ins>requereix més comprensió</ins> de com funciona per evitar certs conflictes.

<ins>**5.**</ins> Explica detalladament el cicle de vida dels components. Fes èmfasi en quan es disparen els hooks OnChanges, OnInit, AfterViewInit i OnDestroy, ja que són els més utilitzats.
- El cicle de vida d'un component és una seqüència d'esdeveniments que es realitzen des de la creació del component, passant per la detecció dels canvis d'aquest (perquè Angular verifica si es canvien les propietats, actualitzant vistes o instàncies) fins a la seva destrucció.
- <ins>**OnChanges**</ins>: es dispara quan la propietat d'entrada canvia.
- <ins>**OnInit**</ins>: es dispara després que Angular inicialitzi totes les propietats del component.
- <ins>**AfterViewInit**</ins>: es dispara després que Angular hagi inicialitzat la vista del component.
- <ins>**OnDestroy**</ins>: es dispara després que Angular hagi destruït el component.