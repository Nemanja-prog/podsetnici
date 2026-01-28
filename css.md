## Komentar
  - /*adad*/

## Selektori u CSS-u
1. Univerzalni
  - * - sve

2. Element 
  - p {} - element

3. Klasa
  - .imeKlase {} - klasa

4. ID
  - #imeID {} - identifikator

5. Grupisanje
  - .klasa1, .klasa2 {} - grupa

6. Vezivanje (više klasa / ID)
  - .klasa1.klasa2 {} - kombinacija

7. Potomak
  - .roditelj .dete
    + Primer:
`<p class="odd adjust-font-size">
 .odd {
  background-color: rgb(255, 167, 167);
  font-family: Verdana, "DejaVu Sans", sans-serif;
}

.adjust-font-size {
  font-size: 24px;
}`

## Uvoz CSS fajla
- @import url(link)

## Boja
1. color - tekst

2. background-color - pozadina
  - Vrednosti:
    + ime - tekst
      * red - ime
    + hex - heksadecimalno
      * #000000 - hex
      * #fff - skraćeni hex 
    + rgb - RGB
      * rgb(0, 0, 0) - rgb
      * rgba (0, 0, 0, 0.5) - transparentnost
    + hsl - HSL 
      * hsl (0, 100%, 50%) - hsl

## Tekst
1. font-family- font
  - Vrednosti:
    + serif - serif
    + sans-serif - bez serif
    + monospace - jednaka širina
    + ime fonta - font
2. font-size - veličina
  - Vrednosti:
    + px - piksel
    + em - relativno
    + rem - root
    + % - procenat

3. font-weight - debljina
  - Vrednosti:
    + 100 - 900 - jačina
    + normal - normalno
    + bold - podebljano
    + lighter - tanje
    + bolder - deblje 

4. text-align - poravnanje
  - Vrednosti:
    + left - levo
    + right - desno
    + center - center
    + justify - poravnato 

5. text-decoration - dekoracija
  - Vrednosti:
    + none - bez
    + underline - podvučeno
    + line-through - precrtano
    + overline - iznad

## Slika
1. width - širina
  
2. height - visina
  - Vrednosti:
   + auto - proporcija
   + px - fiksno
   + % - relativno
   + vw - širina - viewport
   + vh - visina - viewport


## Box model
  Sve je pravougaona kutija.

1. padding - unutrašnji razmak

2. border - ivica

3. margin - spoljašnji razmak
  - Vrednosti: 
   + px - razmak 
   + % - relativno
   + auto - automatski

4. border-style - stil ivice
  - Vrednosti:
   + solid - puna
   + dashed - isprekidana
   + dotted - tačkasta
   + double - dupla
   + none - bez

## display
  - Vrednosti:
   + block - blok
   + inline - linijski (bez dodatnog margin i padding)
   + inline-block - kombinovano (inline ponašanje, block razmaci)
   + none - sakriven

## flex
* slaganje u red ili kolonu
* U roditeljskom bloku koji ima display: flex opcije za flex 
* U dete ide samo: 
  + flex-grow
  + flex-shrink
  + flex-basis
  + order

1. display:flex 
  - flex kontejner
  
2. flex item
  - element unutar flex kontejnera
  
3. flex-grow - rast
  - Vrednosti:
    + 0 - bez rasta
    + 1+ - rast

4. flex-shrink - skupljanje
  - Vrednosti:
    + 0 - bez skupljanja
    + 1+ - skupljanje

5. flex-basis - početna veličina
  - Vrednosti:
    + auto - osnovno
    + px - veličina
    + % - relativno

6. flex-direction putanja
  - Vrednosti:
    + row - red (default)
    + column kolona
    + row-reverse obrnut red
    + column-reverse obrnuta kolona
  
7. flex-wrap - ponašanje
  - Vrednosti:
    + nowrap - bez preloma (default)
    + wrap - prelom
    + wrap-reverse - obrnut prelom
  
8. justify-content glavna osa
      * flex-direction: row po horizontali
      * flex-direction: column po vertikali
  - Vrednosti:
    + flex-start - početak
    + flex-end - kraj
    + center - centar
    + space-between - razmak
    + space-around - oko
    + space-evenly - jednako

9.  align-items - poprečna osa
      * flex-direction: row po vertikali
      * flex-direction: column po horizontali
  - Vrednosti: 
    + stretch - razvlačenje
    + flex-start - vrh
    + flex-end - dno
    + center - centar
    + baseline - tekst

10. gap - razmak između redova i kolone
  - Vrednosti:
    + px - razmak
    + % - relativno

11. Order - redosled
  - Vrednosti:
    + 0 - podrazumevano
    + 1+ - pomeranje