# Affix

Az olyan komponensek, mint a navigáció, gombok stb., rögzíthetők a látható tartományban. Általában hosszú tartalommal rendelkező oldalakhoz használják, a megadott elemeket rögzítik az oldal látható tartományában, hogy segítsenek a gyors működésben.

## Importálás

<!--{include:(components/affix/fragments/import.md)}-->

## Példák

### Alap

<!--{include:`basic.md`}-->

### Felső

<!--{include:`top.md`}-->

### Tároló

Amikor a tároló a látható tartományban van, az elem rögzített. Ha az oldal görgetési tárolója nem a látható tartományban van, akkor az elem nincs rögzítve.

<!--{include:`container.md`}-->

## Tulajdonságok

### `<Affix>`

| Tulajdonság | Típus `(Alapértelmezett)`                         | Leírás                                                                                             |
| -----------| --------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| children   | ReactNode                                       | Rögzített elem.                                                                                    |
| classPrefix| string `('affix')`                              | A komponens CSS osztályának előtagja.                                                              |
| container  | HTMLElement &#124; (() => HTMLElement)          | A konténer megadása. Egy elem csak akkor rögzíthető, ha a konténer a látható tartományban van.   |
| onChange   | (fixed: boolean) => void                        | Visszahívás funkció, amikor a nem rögzített és a rögzített állapot változik.                      |
| top        | number `(0)`                                    | Beállítja a rögzített felső magasságot.                                                           |
