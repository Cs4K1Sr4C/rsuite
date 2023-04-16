# Animáció

Animációs komponensek kezelése

- `<Animation.Fade>`
- `<Animation.Collapse>`
- `<Animation.Bounce>`
- `<Animation.Slide>`
- `<Animation.Transition>`

Ha a Transition nem felel meg az üzleti igényeknek, akkor próbálja ki a ["react-transition-group"-ot](https://github.com/reactjs/react-transition-group)

## Importálás

<!--{include:(components/animation/fragments/import.md)}-->

## Példák

### Fade

<!--{include:`fade.md`}-->

### Collapse

<!--{include:`collapse.md`}-->

### Bounce

<!--{include:`bounce.md`}-->

### Slide

<!--{include:`slide.md`}-->

### Transition

A következő className-eket kell beállítani a Transition-ben, és testre szabni a kapcsolódó CSS-animációt.

```
exitedClassName="custom-exited"
exitingClassName="custom-exiting"
enteredClassName="custom-entered"
enteringClassName="custom-entering"
```

<!--{include:`transition.md`}-->

## Tulajdonsgok

<!--{include:(_common/types/placement4.md)}-->

### `<Animation.Fade>`

| Tulajdonság        | Típus `(Alapértelmezett)`                   | Leírás                                                                                                         |
| ----------------- | ------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| enteredClassName  | string                                      | className hozzáadása a komponenshez a tranzíció befejeződése után                                              |
| enteringClassName | string                                      | className hozzáadása a komponenshez a tranzíció kezdete előtt                                                  |
| exitedClassName   | string                                      | className hozzáadása a komponenshez a tranzíció befejeződése után, amikor már nem jelenik meg a felületen      |
| exitingClassName  | string                                      | className hozzáadása a komponenshez a tranzíció kezdete előtt, amikor a felület eltűnik                        |
| in                | boolean                                     | Ha igaz, akkor a komponens animációja megjelenik                                                                |
| onEnter           | (node?: null, Element, Text) => void        | Visszahívás, amely akkor fut le, mielőtt a komponens megjelenne a tranzícióval                                  |
| onEntered         | (node?: null, Element, Text) => void        | Visszahívás, amely akkor fut le, miután a komponens befejezte a tranzíciót és megjelent a felületen             |
| onEntering        | (node?: null, Element, Text) => void        | Visszahívás, amely akkor fut le, amikor a komponens megjelenik a tranzícióval                                  |
| onExit            | (node?: null, Element, Text) => void        | Visszahívás, amely akkor fut le, mielőtt a komponens eltűnik a tranzícióval                                     |
| onExited          | (node?: null, Element, Text) => void        | Visszahívás, amely akkor fut le, miután a komponens befejezte a tranzíciót és már nem jelenik meg a felületen  |
| onExiting         | (node?: null, Element, Text) => void        | Visszahívás, amely akkor fut le, amikor a komponens eltűnik a tranzícióval                                      |
| timeout           | number `(300)`                              | Az animációs tranzíció késleltetési ideje                                                                       |
| transitionAppear  | boolean                                     | Az átmenetek bekapcsolása az inicializálásnál                                                                   |
| unmountOnExit     | boolean                                     | A komponens eltávolítása a DOM-ból, amikor befejeződött a tranzíció                                           |
| 

### `<Animation.Collapse>`

| Tulajdonság        | Típus `(Alapértelmezett)`                                | Leírás                                                             |
| ----------------- | -------------------------------------------------------- | ----------------------------------------------------------------- |
| dimension         | 'magasság'&#124;'szélesség'&#124;() => ('magasság'&#124;'szélesség') | Beállítja a behajtás méretét.                                       |
| enteredClassName  | sztring `('collapse in')`                                 | Class nevet ad hozzá a komponenshez, amikor befejeződött az animáció.   |
| enteringClassName | sztring `('collapsing')`                                  | Class nevet ad hozzá a komponenshez, amikor elkezdődik az animáció.       |
| exitedClassName   | sztring `('collapse')`                                    | Class nevet ad hozzá a komponenshez, amikor befejeződött az animáció. |
| exitingClassName  | sztring `('collapsing')`                                  | Class nevet ad hozzá a komponenshez, amikor elkezdődik az animáció.      |
| getDimensionValue | () => szám                                               | Egyéni méret érték.                                                |
| in                | logikai                                                  | Ha igaz, az animáció megjelenik.                                    |
| onEnter           | (node?: null, Element, Text) => void                     | Visszahívás, amelyet meghív a komponens az animáció előtt.                |
| onEntered         | (node?: null, Element, Text) => void                     | Visszahívás, amelyet meghív a komponens az animáció befejeződése után.   |
| onEntering        | (node?: null, Element, Text) => void                     | Visszahívás, amelyet a komponens az animáció elkezdésekor hív meg.           |
| onExit            | (node?: null, Element, Text) => void                     | Visszahívás, amelyet a komponens az animáció előtt hív meg.         |
| onExited          | (node?: null, Element, Text) => void                     | Visszahívás, amelyet a komponens az animáció befejeződése után hív meg.   |
| onExiting         | (node?: null, Element, Text) => void                     | Visszahívás, amelyet a komponens az animáció elkezdésekor hív meg.          |
| role              | sztring                                                   | HTML szerepe                                                       |
| timeout           | szám `(300)`                                            | Animáció átmeneti késleltetési ideje                                |
| transitionAppear  | logikai                                                  | Átmenetek bekapcsolása a kezdeti megjelenítéskor                     |
| unmountOnExit     | logikai                                                  | Az elem leválasztása az animáció befejeződése után                    |

### `<Animation.Slide>`

| Tulajdonság        | Típus `(Alapértelmezett)`           | Leírás                                                             |
| ----------------- | ------------------------------------ | ------------------------------------------------------------------ |
| enteredClassName  | string                               | A className hozzáadása a komponenshez, amikor a tranzíció befejeződött |
| enteringClassName | string                               | A className hozzáadása a komponenshez, amikor a tranzíció elkezdődik |
| exitedClassName   | string                               | A className hozzáadása a komponenshez, amikor a tranzíció befejeződött |
| exitingClassName  | string                               | A className hozzáadása a komponenshez, amikor a tranzíció elkezdődik |
| in                | boolean                              | Ha igaz, akkor az animáció megjelenik                              |
| onEnter           | (node?: null, Element, Text) => void | Visszahívás, amely akkor hívódik meg, mielőtt a komponens belép     |
| onEntered         | (node?: null, Element, Text) => void | Visszahívás, amely akkor hívódik meg, miután a komponens belépett    |
| onEntering        | (node?: null, Element, Text) => void | Visszahívás, amely akkor hívódik meg, amikor a komponens belép       |
| onExit            | (node?: null, Element, Text) => void | Visszahívás, amely akkor hívódik meg, mielőtt a komponens kilép      |
| onExited          | (node?: null, Element, Text) => void | Visszahívás, amely akkor hívódik meg, miután a komponens kilépett    |
| onExiting         | (node?: null, Element, Text) => void | Visszahívás, amely akkor hívódik meg, amikor a komponens kilép       |
| timeout           | number `(300)`                       | Az animáció tranzíciós késleltetési ideje                            |
| transitionAppear  | boolean                              | Az áttűnések bekapcsolása a kezdeti megjelenítéskor                 |
| unmountOnExit     | boolean                              | Az összetevő eltávolítása a kilépéskor                              |
| placement         | Placement `('right')`                | Az összetevő elhelyezkedése                                         |

### `<Animation.Transition>`

| Tulajdonság       | Típus `(Alapérték)`                   | Leírás                                                             |
| ----------------- | ------------------------------------ | ----------------------------------------------------------------- |
| enteredClassName  | string                               | Osztálynevet ad hozzá az elemhez, miután az átmenet befejeződött   |
| enteringClassName | string                               | Osztálynevet ad hozzá az elemhez, amikor az átmenet elkezdődik     |
| exitedClassName   | string                               | Osztálynevet ad hozzá az elemhez, miután az átmenet befejeződött    |
| exitingClassName  | string                               | Osztálynevet ad hozzá az elemhez, amikor az átmenet elkezdődik     |
| in                | boolean                              | Ha igaz, az animáció megjelenik.                                   |
| onEnter           | (node?: null, Element, Text) => void | Visszahívódás, amelyet a komponens átmenete előtt hívunk meg        |
| onEntered         | (node?: null, Element, Text) => void | Visszahívódás, amelyet a komponens átmenete befejeződése után hívunk meg |
| onEntering        | (node?: null, Element, Text) => void | Visszahívódás, amelyet a komponens átmenete kezdetén hívunk meg      |
| onExit            | (node?: null, Element, Text) => void | Visszahívódás, amelyet a komponens átmenete előtt hívunk meg        |
| onExited          | (node?: null, Element, Text) => void | Visszahívódás, amelyet a komponens átmenete befejeződése után hívunk meg |
| onExiting         | (node?: null, Element, Text) => void | Visszahívódás, amelyet a komponens átmenete kezdetén hívunk meg      |
| timeout           | number`(1000)`                       | Animációs átmenet késleltetési ideje                                 |
| transitionAppear  | boolean                              | Kapcsolja be az átmeneteket az inicializáláskor                      |
| unmountOnExit     | boolean                              | Az elem leszerelése az átmenet befejezése után                       |
