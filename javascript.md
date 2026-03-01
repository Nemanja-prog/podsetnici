## <script>
* JavaScript kod.
  ### Atribut src eksterno i defer
* `defer` - čeka da se HTML učita pre JavaScript-a
  Primer koji je preporučen:
  `<script src="javascript.js" defer></script>`

## Greške
1. `ReferenceError` promenljiva nedeklarisana i/li urađena i/li naziv loše napisan (poruke:
 1. ReferenceError: x is not defined
 2. ReferenceError: can't access lexical declaration 'X' before initialization)
2. `SyntaxError` kod nije ukucan po pravilima JavaScript-a
3. `TypeError` iz više razloga, neki su:
  - Operand ili argument u funkciji su nekompatibilni sa tipom koji se očekuje od tog operanda ili funkcije
  - Modifikovanje vrednosti koja ne može da se menja
  - Korišćenje vrednosti na nekompatibilan način
   * Primer česte poruke te greške: `str1.push is not a function`
   * Proveriti tip podatka za metodu ili operaciju
  ### Delovi
  1. Tip greške
  2. Ime fajla sa greškom i red linije (at script.js:4), može i da pokaže kolonu (karakter) (at script.js:4:13)
  3. stack trace - kada je pokazana greška i koje funkcije su je dovele
  ### Saveti za rešavanje grešaka
  1. Reći će šta nije u redu sa kodom
  2. Pretraži Internet
  3. Koristi debugger
  4. Koristi `console.log()`
  + Razlika između greške i upozorenja:
  1. Greška zaustavlja, upozorenje javlja potencijalnu grešku
  2. Upozorenje su u žuto, greške u crveno

## Načini Otvaranja DevTools-a
1. Meni > More Tools > (Web) Developer Tools
2. Desni Klik Inspect
3. `F12`
4. `Ctrl + Shift + C`

## console.log
* Štampanje u developer console.
  ### Primer:
  `console.log('Hello, World!');`

## Promenljive:
  ### `let`
  #### Primer:
  `let firstName = "John";
    console.log(firstName);`
    Rezultat: John
  * Može da menja vrednost.
  #### Primer:
  `let age = 11;
  console.log(age); // 11
  age = 54;
  console.log(age);`
  Rezultat: 54

  ### `const`
  * Ne može da menja vrednost.
  #### Primer:
  `const pi = 3.14;
  pi = 10;
  console.log(pi);`
  Greška `Uncaught TypeError`
- NE koistiti `var` zbog:
  1. Zamenjen je sa `let` i `const`
  2. Može da pravi bagove
  3. ima `function scope` - Dostupnost

### Brojevi
  * Redosled operacija:
  1. Zagrade
  2. Deljenje i množenje sa leva na desno
  3. Oduzimanje i sabiranje sa leva na desno
   
## Tipovi podataka:
  ### String
  * Tekst pod `" "`, `' '` ili ``.
  * Prva pozicija je 0, a druga 1.
  * Ne može da se mešaju navodnici, samo u ovoj situaciji "Hello 'world'".
    #### Primer:
    `const string = "The revolution will not be televised.";
     console.log(string);`
     Rezultat: The revolution will not be televised.
  * Preporučljivo je koristiti ``.
  * Može da se ubaci promenljiva tj. konkatenacija.
    #### Primeri:
    `const name = "Chris";
     const greeting = `Hello, ${name}`;
     console.log(greeting);`
     Rezultat: Hello, Chris

    `const one = "Hello, ";
     const two = "how are you?";
     const joined = `${one}${two}`;
     console.log(joined);`
     Rezultat: Hello, how are you?
  * Poštuje razmake.
    #### Primer:
    `const newline = One day you finally knew
what you had to do, and began,`;
     console.log(newline);` 
     Rezultat: One day you finally knew
     what you had to do, and began,

  * `\n` line break.
    #### Primer:
    `const newline2 = "One day you finally knew\nwhat you had to do, and began,";
    console.log(newline2);`
    Rezultat: One day you finally knew
    what you had to do, and began,
  * Ubacivanje navodnika
    #### Primeri:
    1. `const goodQuotes1 = 'She said "I think so!"';`
    2. `const goodQuotes2 =` `She said "I'm not going in there!"`;
    3. `const bigmouth = 'I\'ve got no right to take my place…';
    console.log(bigmouth);`
  * Kad je tu tekst i broj, broj postaje deo teksta.
    #### Primer:
    `const coolBandName = "Front ";
     const number = 242;
     console.log(coolBandName + number);`
     Rezultat: "Front 242"

  * `Number()` pretvara u broj.
    #### Primer:
    `const myString = "123";
     const myNum = Number(myString);
     console.log(typeof myNum);`
     Rezultat: number

  * `String()` pretvara u string.
    #### Primer:
    `const myNum2 = 123;
     const myString2 = String(myNum2);
     console.log(typeof myString2);`
     Rezultat: string

    + Metode:
    1. `.length` - dužina
    2. `.charAt()` - karakter na toj poziciji u stringu
    3. `.charCodeAt()` - kod karaktera na toj poziciji u stringu
    4. `codePointAt()` - vraća code point na toj poziciji u stringu
    5. `.at()` - vraća deo teksta na toj poziciji u stringu (može i negativna vrednost)
    6. `[]` - svojstva
      ##### Napomena:
       - string izgleda kao niz
       - ako karakter nije pronađen vraća undefined
       - Samo je za čitanje
    7. `.concat()` - spaja dva ili više stringa
    8. `.slice()` - izvlači deo stringa i vraća izvučeni deo
      #### Parametri:
       *  Startna pozicija
       *  Krajnja pozicija (nije uključena u toku izvlačenja)
      ##### Napomena:
      - Ako se ne stavi drugi parametar, metoda seče ostatak stringa
      - Ako je parametar negativan, broji se od kraja stringa
      ###### Primer:
      `let text = "Apple, Banana, Kiwi";
       let part = text.slice(-12, -6);
       console.log(part);`
       Rezultat: Banana

    9.  `.substring()` - sličan `.slice()` metodi, razlika je ako je broj na početku i kraju manji od 0 tretiraju se kao 0
      ##### Napomena:
      - Ako se ne stavi drugi parametar, metoda seče ostatak stringa
    10. `.toUpperCase()` - velika slova
    11. `.toLowerCase()` - mala slova
    12. `.isWellFormed()` - vraća true ako je string dobro formatiran tj. da nije "lone surrogates" (usamljeni surogat) (nije deo validnih parova u UTF-16 enkodiranju)
    13. `.toWellFormed()` - svi "lone surrogates" zamenjeni sa zamenjujućim Unicode karakterom
    14. `.trim()` - uklanja prazan prostor
    15. `.trimStart()` - uklanja prazan prostor SA početka stringa
    16. `.trimEnd()` - uklanja prazan prostor SA kraja stringa
    17. `.padStart()` - dodaje sa početka stringa nove elemente dok ne dostigne granicu
      ##### Primer:
      `let text = "5";
       let padded = text.padStart(4,"0");
       console.log(padded)`
       Rezultat: 0005

    18. `.padEnd()` - dodaje sa kraja stringa nove elemente dok ne dostigne granicu
      ##### Napomena:
      - Da bi radilo sa brojevima, broj mora PRVO da se pretvori u string
      ###### Primer:
      `let text = "5";
       let padded = text.padEnd(4,"0");
       console.log(padded)`
       Rezultat: 5000

    19. `.repeat()` - vraća kopije stringa onoliko puta koliko je dato
      #### Parametar:
      * count - broj
    20. `.replace()` - Menja datu vrednost sa drugom vrednošću u stringu
      ##### Napomena:
      - Zamenjuje samo prvu vrednost sa kojom se poklapa
      - on je case sensitive (ako je ukucana velikim slovom, tražiće da je baš tako ukucan)
      ###### Primer:
      `let text = "Please visit Microsoft!";
       let newText = text.replace("Microsoft", "W3Schools");
        console.log(newText);`
        Rezultat: Please visit W3Schools!

    21. `.replaceAll()` - kucanje regularnog izraza umesto stringa za zamenu
      ##### Napomena:
      - Kad je parametar regularni izraz, /g mora da stoji
      ###### Primer:
      `text = text.replaceAll(/Cats/g,"Dogs");
       console.log(text);`
       Rezultat: Dogs are awesome;

    22.  `.split()` - pretvara string u niz
      ##### Parametar:
      * znak za razdvajanje (", ", " ", "|")
      ##### Napomena:
      - Sve string metode vraćaju nov string, ne modifikuju originalni
      - 
  ### Number
  - To su `Integer` i `Float`
  - Operacije: `*`, `/`, `-`, `+`, `%`
  - Spada i `Infinity`, `-Infinity` i `NaN` (greška Not a Number)
  #### Provera za Nan:
  `isNaN("hello"); // true
  Number.isNaN(NaN); // true`

  ### BigInt
  - Retko se koriste
  - vrednost je veća od MAX_SAFE_INTEGER
  - Nema ograničenje (granica je od `9007199254740991` do `-9007199254740991` za bezbedan opseg)

  ### Boolean (logički operator)
  - `true` ili `false`

  ### null
  - Specijalan tip podatka
  - Predstavlja `ništa`, `prazno` ili `nepoznata vrednost`
  
  ### undefined
  - Još jedan specijalan tip podatka
  - Predstavlja `nije data vrednost` 
  - Kad se definiše promenljiva bez vrednosti
  - Može da se promenljivi da undefined vrednost ali se NE PREPORUČUJE
    #### Primer:
    `let age = undefined;
     console.log(age);`
     Rezultat: undefined

  ### Objekti i simboli
  - `Objekti` su još jedan specijalan tip podatka
  - Skladište kolekciju podataka i kompleksnih entiteta
  - `Simboli` za pravljenje jedinstvenih identifikatora za `objekte`
 
  ### typeof
  To je operator koji vraća tip podatka
    #### Sintakse:
    - `typeof x`
    - `typeof(x)`
    ##### Primer:
      `typeof undefined // "undefined"

       typeof 0 // "number"

       typeof 10n // "bigint"

       typeof true // "boolean"

       typeof "foo" // "string"

       typeof Symbol("id") // "symbol"

       typeof Math // "object"

       typeof null // "object"

       typeof alert // "function"`

## Upoređivanja:
  1. `>` veće, `<` manje
  2. `>=` veće ili jednako, `<=` manje ili jednako
  3. `==` jednako, `!=` nije jednako
  4. `===` striktno jednako (podatak je jednak sa drugim i ISTOG tipa) - Preporuka
  5. `!==` striktno nejednako (podatak nije jednak sa drugim i(li) NISU ISTOG tipa) - Preporuka
  +  Rezultati su Boolean vrednosti: `true` (1) ili `false` (0)
  + Logički operatori:
  1. `||` (OR(ILI))
  2. `&&` (AND(I))
  3. `!` (NOT(NIJE))
  4. `??` (nullish coalescing) - reaguje samo na `null` i `undefined`
  - `||` vraća prvu `truthy` vrednost ili poslednju ako su sve `falsy` i često se koristi u `IF` kondicionom izrazu
  - `&&` je `true` kad su obe vrednosti `true`
  - `!` pretvara tj. `true` postaje `false`, a `false` postaje `true`
  - Falsy vrednosti:
  1. `false`
  2. `0`
  3. `""`
  4. `null`
  5. `undefined`
  6. `NaN`

## Kondicioni uslovi:
  1. `if`
   - Uslov
   - Kada je `true` izvršava kod u bloku
    ##### Sintaksa:
    `if (uslov) {kod}`
    ###### Primer:
    `if (year == 2015) {
     alert( "That's correct!" )};`

  2. `else`
   -  Opcioni uslov
   -  Uslov kada je `if` `false`
    ##### Sintaksa:
    `if (uslov) {kod} else {opcioni kod}`
    ###### Primer:
    `if (year == 2015) {
     alert( 'You guessed it right!' );
     } else {
     alert( 'How can you be so wrong?' ); // any value except 2015
     }`

  3. `else if`
   - Varijacije uslova kada je `if` false
   - Ide pre `Else`
    ##### Sintaksa:
    `if (uslov) {kod} else if(drugi uslov) {drugi kod} else {opcioni kod}`
    ###### Primer:
    `if (year < 2015) {
    alert( 'Too early...' );
    } else if (year > 2015) {
    alert( 'Too late' );
    } else {
    alert( 'Exactly!' );
    }`

  4. Ternarni operator
   - Zamena za prethodne kondicione uslove
   - Ako je tačna `value1` se vraća, ako nije vraća se `value2`
    ##### Sintaksa:
    `result = condition ? value1 : value2`
    ###### Primer:
    `let accessAllowed = (age > 18) ? true : false;`

  5. `Switch`
   - Menja više `if` provera
   - Ima jedan ili više `case` i opcioni `default`
    ##### Sintaksa:
    `switch(x) {
     case 'value1':  // if (x === 'value1')
     ...
     [break]

     case 'value2':  // if (x === 'value2')
     ...
     [break]

     default:
     ...
     [break]
     }`
    ###### Primer:
    `let a = 2 + 2;

     switch (a) {
     case 3:
     alert( 'Too small' );
     break;
     case 4:
     alert( 'Exactly!' );
     break;
     case 5:
     alert( 'Too big' );
     break;
     default:
     alert( "I don't know such values" );
    }`

    - Nekoliko varijanti `case` koji dele isti kod mogu da se grupišu
    ###### Primer:
    let a = 3;

    switch (a) {
    case 3:
    alert('Right!');
    break;

    case 4:
    case 5:
    alert('Wrong!');
    alert("Why don't you take a math class?");
    break;

    default:
    alert('The result is strange. Really.');
    }

## Funkcija
  #### Sintaksa:
  `function imeFunkcije(parametar) {
    kod
  }`
  `imeFunkcije(parametar tj. argument)` - pozivanje
  * Parametar unutar zagrade funkcije (vrednosti koji se daju)
  ##### Primer:
    `function favAnimal(animal) {
     return animal;
     }
     const message = favAnimal('Goat');`
    - Može i ovo:
    `console.log(favAnimal('Goat'));` 

## Petlje
  * Ponavljanje koda više puta
  * GLEDATI DA SE BROJAČ POVEĆAVA ILI SMANJUJE DA BI USLOV KASNIJE POSTAO FALSE!!!
  * Vrste:
    - `For`
    - `While`
  * Petlja kroz kolekciju podataka (npr. Array):
    - `For...of`
    - `map()`
    - `filter()`
    + `map()` i `filter()` često sa parametrom funkcije
  ### For petlja
    #### Sintaksa:
    `for (inicijalizator; uslov; poslednji izraz){
     kod
     }`
  + Sadrži:
   1. for
   2. inicijalizator - promenljiva tj. brojač
   3. uslov - kada da se petlja zaustavi
   4. poslednji izraz - radi svaki put kada je jedna petlja završena (povećava ili smanjuje brojač dok više nije `true`)
   5. kod koji će raditi
    ##### Primer:
    `for (let i = 1; i < 10; i++){
     console.log("Hello");
     }`

    ##### Primer for..of petlje:
    `const cats = ["Leopard", "Sarvel", "Jaguar"];
     for (const cat of cats){
     console.log(cat);
     }`

  * `break` - izlaz iz petlje pre njenog kraja 
  * `break <labelName>` izlaz iz unutrašnje petlje
  * `continue` - preskakanje trenutne iteracije petlje
  * `continue <labelName>` preskakanje iteracije u unutrašnjoj petlji
  * NE MOŽE UNUTAR TERNARNOG OPERATORA JER SU NAREDBE!
  * Može bilo koji deo `For` petlje da se preskoči
  ### While i do...while petlja
    #### Sintaksa:
    `inicijalizator
      while (uslov) {
      kod
      poslednji izraz
      }`
  * Veoma slična `For` petlji, samo je promenljiva brojač pre petlje i poslednji izraz je unutar petlje, uslov je u zagradi
    ##### Primer:
    `const cats = ["Pete", "Buggles", "Jasmine"];
     let i = 0;
     while (i < cats.length){
     console.log("Hi");
     i++;
     }`

  * Vitičaste zagrade nisu potrebne za kod u jednoj liniji
  ### Do...while je sličan
    #### Sintaksa:
    `inicijalizator
     do {kod
     poslednji izraz
     } while (uslov)`
    * Kod unutar do...while petlje će se uvek izvršiti barem jednom
    * Inicijalizator ide prvi, ključna reč direktno nasleđuje kod u vitičastim zagradama i poslednji izraz
    * Uslov dolazi posle kode unutar petlje i ako je `true` ponovo će izvršiti petlju
    ##### Primer:
    `const cats = ["Pete", "Buggles", "Jasmine"];
     let i = 0;
     do {
     if(i === cats.length - 1){
      console.log("Hi");
      }
      i++;
      } while (i < cats.length);`
