## Skraćenica za html u Visual studio code
1. Kucaj ! i pritisni Enter

## Skraćenica za komentar
1. Pritisni Ctrl i /

## Bezbednost
1. Koristi target="_blank" i rel="noreferrer"

## Relativna pretraga sa ./
1. ./images/dog.jpg

## Odlazak u roditeljski folder ../
1. ../images/dog.jpg

## Globalni atributi
1. id - identifikacija
   + ime - identitet
  
2. class - klasa
   + ime - stil
  
3. lang - jezik
   + en - engleski
   + sr - srpski

## Uvek stoji na vrhu
1. `<!DOCTYPE html>`

## `<html>`
### lang - jezik
   + en - engleski
   + sr - srpski

## Struktura
1. `<!DOCTYPE html>`
2. `<html>`
3. `<head>`
4. `<body>`

## head (ne vidi se)
+ Podaci o sajtu:
1. `<meta>` 
    ### `<meta>`: 
    - charset - kodiranje
        + UTF-8
    - name - tip
        + description - opis
        + keywords - ključne reči
        + author - autor
        + viewport - responzivnost 
    - content - vrednost
        + tekst - vrednost
  
1. `<title>` naslov u tabu

2. `<link>` povezivanje sa drugim fajlom
    ### `<link>`: 
    - rel - odnos
        + stylesheet - stilovi
        + icon - ikona
    - href - putanja
        + putanja - lokacija

## body (vidljivo)
+ Zatvoreni tagovi:

1. `<h1>` naslov (do `<h6>`)
* Samo jedan `<h1>`

2. `<p>` paragraf

3. `<strong>` važan tekst

4. `<em>` kurziv (naglašen tekst)

5. `<ul>` neuređena lista

6. `<ol>` uređena (brojčana) lista
    ### `<ol>`:
    - type - tip
        + 1 - brojevi
        + A - velika slova
        + a - mala slova
        + I - rimski
        + i - mali rimski
    - start - početak
        + broj - početak 

7. `<li>` stavka u listi

8. `<a>` link
    ### `<a>`:
    - href - putanja
        + url - destinacija
        + #id - sidro
    - target - otvaranje
        + _self - isto
        + _blank - novo
        + _parent - roditelj
        + _top - vrh
    - rel - bezbednost
        + noreferrer - privatnost
        + noopener - sigurnost

9.  `<div>` kontejner
    ### `<div>`:
    - id - identifikacija
        + ime - identitet
    - class - klasa
        + ime - stil

+ Otvoreni tagovi:

1. `<img>` slika
    ### `<img>`: 
      - src - izvor
        + putanja - izvor
      - alt - opis
        + opis - pristupačnost
      - width - širina
        + broj
      - height - visina
        + broj