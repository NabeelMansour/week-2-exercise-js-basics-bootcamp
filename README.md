# Övning: JavaScript Basics Bootcamp

## Syntax n stuff

### Datatyper
**1** Vilka datatyper finns det i JS?

**2** Är följande if sats *true* eller *false*?

```javascript
let a = 1;
let b = '1';
if(a == b) // true or false
```

**3** Vad är den *tekniska* skillnaden på dessa två deklarationer?

```javascript
let name = 'Greta Thunberg';
var name = 'Greta Thunberg';
```

**4** Skapa variabeln ```myStr``` som du tilldelar en sträng, ```myNum``` som du tilldelar ett nummer, och ```myBool``` som du tilldelar en boolean.

**5** Hur tar man reda på vad en variabel har för datatyp? Testa på variablerna från övning 4.

**6** Skriv ett program som frågar användaren efter två tal och sparar dem i variabler. Sedan ska det skriva ut talens summa, differens och produkt. Du kan använda dig av .prompt()-funktionen för att ta input från användaren.

### Block 

**7** Vilken av följande syntax visar ett ```kodblock```?

```javascript
[] // A 
() // B
{} // C
```

**8** Vad i följande kod är ```blocket``` som *exekveras*?

```javascript
function hello(){
  console.log("Hello")
}
function goodbye(){
  console.log("Goodbye")
}
hello()
```

**9**
Vad kommer stå i ```console.log()```?

```javascript
var greeting = 'Good bye world!';

{
    let greeting = 'Hello World';
}

console.log(greeting);
```

### Strings

String-objektet innehåller en rad olika fördefinierade funktioner. Ni kommer att behöva använda några av nedanstående till Strings-övningarna. Läs på om det själva.

* .concat()
* .charAt()
* .substring()
* .replace()
* .toLowerCase()
* .toUpperCase()
* .toString()
* .trim()
* .split()
* .includes()

**10** Vilken av följande syntax är korrekt sätt att skriva strängar.

```javascript
"Hello World" // A
'Hello World' // B
`Hello World` // C
```

**11** Räkna antal tecken i strängen nedan.

```js
let sentence = "If you're having code problems I feel bad for you son. I got 99 problems, but a glitch ain't one."
```

**12** Tilldela variabeln ```myName``` ett värde, och använd sedan strängkonkatenering för att stoppa in den i meningen istället för ```N``` .

```javascript
let myName = '<Ditt namn>' 
`Hej N din gamle knasboll!`
```

**13** Gör en *template string* där ```N``` ersätts med variabeln ```myName```.

```javascript
let myName = '<Ditt namn>' 
`Hej N din gamle knasboll!`
```

**14** Gör om uppgift 13, men låt istället användaren själv ange sitt namn med hjälp av .prompt()-funktionen. Skriv sedan ut meningen med hjälp av .alert()-funktionen.

```javascript
let myName = INPUT från användaren 
`Hej N din gamle knasboll!`
```

**15** Gör om alla tecken i strängen nedan till stora bokstäver.

```javascript
let sentence = "They see me coding, debugging"; 
```

**16** Plocka ut de 4 första tecknen i strängen nedan för att ta reda på vilket år det är. Använd sedan .concat() för att skriva ut ```sentence```.

```javascript
let date = "20250106"; 
let sentence = "2025 ska jag lära mig att koda!";
```

**17** Undersök om variabeln ```sentence``` nedan innehåller ordet ```debug```.

```javascript
let sentence = "You only get one loop, don't miss your chance to debug, 'cause an infinite loop can break your runtime.";
```

**18** Ta bort alla kommatecken från variabeln ```sentence``` nedan.

```javascript
let sentence = "I said a git push, the puller, the puller to the git git push, and the commit.";
```

### Math Object

Innan du ger dig på dessa övningar kan du med fördel besöka MDNs [Math Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math).

**19** Arunda talet ```1337.51``` *nedåt* till närmaste heltal med hjälp av *Math object*.

**20** Arunda talet ```1337.48``` *uppåt* till närmaste heltal med hjälp av *Math object*.

**21** Arunda talet ```1337.497``` *till närmaste heltal* med hjälp av *Math object*.

**22** Slumpa fram ett tal mellan 1 - 100.

### Selektioner / Villkor

**23** Skriv ett program som frågar användaren efter ett lösenord. Hitta på ett hemligt lösenord och spara det i en variabel. När användaren har skrivit in ett ord ska programmet jämföra med det sparade lösenordet och skriva ut om det var rätt eller inte. Använd en if-sats.

**24** Skriv ett program som frågar användaren efter ett tal. Det ska skriva ut om talet är mindre än 100, lika med 100 eller större.

**25** För att åka en viss karusell på Liseberg behöver ditt barn vara minst 10 år gammal, och vara längre än 135 cm lång. Skriv ett program där användaren kan ange sitt barns ålder och längd, och ta sedan reda på om barnet får åka karusellen. Levelup: om barnet inte får åkakarusellen, förklara då exakt vilken anledningen är.

### Iterationer

**26** Skapa en ```for-loop``` som skriver ut talen 1 till 100 i konsollen.

**27** Gör om övning 26, men använd denna gången en ```while-loop```. Vilka justerngar behöver du göra?

**28** Skapa en ```for-loop``` så körs 100 gånger. Inuti varje loop skall du slumpa fram ett tal mellan 1 - 100. Räkna sedan ut medelvärdet av dina 100 slumpningar.

**29** Skapa en ```while-loop``` som körs tills du lyckats slumpa fram ett valt tal mellan 1 - 100. Levelup: håll koll på hur många gånger du slumpat och skriv sedan ut detta i konsollen.

**30** Be användaren mata in sitt födelsedatum enligt (YYYYMMDD-XXXX). Använd en ```while-loop``` som körs tills användaren har angett korrekt antal tecken. Skriv sedan ut användarens fyra sista siffror i konsollen.

```javascript
let correctInput = false;
while() {
  let birthdate = prompt("Ange födelsedatum i formatet (YYYYMMDD-XXXX)");
}
```








