# Övning: JavaScript Basics Bootcamp

## Syntax n stuff

### Datatyper
**1** Vilka datatyper finns det i JS?

String
Number
Boolean
Object
Undefined / Null
Symbol

**2** Är följande if sats *true* eller *false*?

```javascript
let a = 1;
let b = '1';
if(a == b) // true or false
true
```

**3** Vad är den *tekniska* skillnaden på dessa två deklarationer?

```javascript
let name = 'Greta Thunberg';
var name = 'Greta Thunberg';
let är block scoped, medan var är function scoped så att den är tillgänglig i hela funktionen. Var är också hoisted. 
```

**4** Skapa variabeln ```myStr``` som du tilldelar en sträng, ```myNum``` som du tilldelar ett nummer, och ```myBool``` som du tilldelar en boolean.
let myStr = 'Hello'
let myNum = 10
let myBool = true
**5** Hur tar man reda på vad en variabel har för datatyp? Testa på variablerna från övning 4.
typeof
**6** Skriv ett program som frågar användaren efter två tal och sparar dem i variabler. Sedan ska det skriva ut talens summa, differens och produkt. Du kan använda dig av .prompt()-funktionen för att ta input från användaren.
function talRäknare(){
  let förstaTal = Number(prompt('Knappa in ett nummer'))
  let andraTal = Number(prompt('Knappa in ett annat nummer'))

  console.log(förstaTal + andraTal)
  console.log(förstaTal - andraTal)
  console.log(förstaTal * andraTal)
}
talRäknare()
### Block 

**7** Vilken av följande syntax visar ett ```kodblock```?

```javascript
[] // A 
() // B
{} // C

C
```

**8** Vad i följande kod är ```blocket``` som *exekveras*?

```javascript
function hello(){
  console.log("Hello")
}
function goodbye(){
  console.log("Goodbye")
}
hello() // Den här
```

**9**
Vad kommer stå i ```console.log()```?

```javascript
var greeting = 'Good bye world!';

{
    let greeting = 'Hello World';
}

console.log(greeting);
Det kommer stå :
'Good bye world!'
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
Svar: Alla
```

**11** Räkna antal tecken i strängen nedan.

```js
let sentence = "If you're having code problems I feel bad for you son. I got 99 problems, but a glitch ain't one."
sentence.length
```

**12** Tilldela variabeln ```myName``` ett värde, och använd sedan strängkonkatenering för att stoppa in den i meningen istället för ```N``` .

```javascript
let myName = 'Nabeel' 
`Hej ` + myName + ' ' + `din gamle knasboll!`
```

**13** Gör en *template string* där ```N``` ersätts med variabeln ```myName```.

```javascript
let myName = 'Nabeel' 
`Hej ${myName} din gamle knasboll!`
```

**14** Gör om uppgift 13, men låt istället användaren själv ange sitt namn med hjälp av .prompt()-funktionen. Skriv sedan ut meningen med hjälp av .alert()-funktionen.

```javascript
let myName = prompt('Vad heter du? ')
`Hej ${myName} din gamle knasboll!`
```

**15** Gör om alla tecken i strängen nedan till stora bokstäver.

```javascript
let sentence = "They see me coding, debugging";
sentence.toUpperCase() 
```

**16** Plocka ut de 4 första tecknen i strängen nedan för att ta reda på vilket år det är. Använd sedan .concat() för att skriva ut ```sentence```.

```javascript
let date = "20250106"; 
let sentence = "2025 ska jag lära mig att koda!";

let date = "20250106";
let sentence = "2025 ska jag lära mig att koda!";
let year = date.slice(0, 4)
sentence.replace('2025', year)

console.log(sentence)
```

**17** Undersök om variabeln ```sentence``` nedan innehåller ordet ```debug```.

```javascript
let sentence = "You only get one loop, don't miss your chance to debug, 'cause an infinite loop can break your runtime.";
sentence.includes('debug')
```

**18** Ta bort alla kommatecken från variabeln ```sentence``` nedan.

```javascript
let sentence = "I said a git push, the puller, the puller to the git git push, and the commit.";
console.log(sentence.replaceAll(',', ' '))
```

### Math Object

Innan du ger dig på dessa övningar kan du med fördel besöka MDNs [Math Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math).

**19** Arunda talet ```1337.51``` *nedåt* till närmaste heltal med hjälp av *Math object*.
Math.floor(1337.51)
**20** Arunda talet ```1337.48``` *uppåt* till närmaste heltal med hjälp av *Math object*.
Math.ceil(1337.48)

**21** Arunda talet ```1337.497``` *till närmaste heltal* med hjälp av *Math object*.
Math.round(1337.597)
**22** Slumpa fram ett tal mellan 1 - 100.
Math.floor(Math.random() * 100) + 1
### Selektioner / Villkor

**23** Skriv ett program som frågar användaren efter ett lösenord. Hitta på ett hemligt lösenord och spara det i en variabel. När användaren har skrivit in ett ord ska programmet jämföra med det sparade lösenordet och skriva ut om det var rätt eller inte. Använd en if-sats.

let lösenOrd = 'Arsenal'
let svarPåLösenOrd = prompt('Gissa det hemlig lösenord? ')

if(svarPåLösenOrd === lösenOrd){
  console.log('Du har gissat rätt')
} else {
  console.log('Fel gissat, försök igen')
}

**24** Skriv ett program som frågar användaren efter ett tal. Det ska skriva ut om talet är mindre än 100, lika med 100 eller större.

let favoriteNumber = prompt('What is your favorite number? ')
if(favoriteNumber < 100){
  console.log('talet är mindre än 100')
} else if(favoriteNumber === 100){
  console.log('talet är lika med 100')
} else{
  console.log('talet är större än 100')
}

**25** För att åka en viss karusell på Liseberg behöver ditt barn vara minst 10 år gammal, och vara längre än 135 cm lång. Skriv ett program där användaren kan ange sitt barns ålder och längd, och ta sedan reda på om barnet får åka karusellen. Levelup: om barnet inte får åkakarusellen, förklara då exakt vilken anledningen är.

let personÅlder = prompt('Hur gammal är du ? ')
let personLängd = prompt('Hur lång är du i cm ? ')

if(personÅlder >= 10 && personLängd >= 135){
  console.log('Du kan åka karusellen')
} else if(!(personÅlder >= 10 && personLängd >= 135)){
  console.log('Du måste vara 10 år gammal och 135cm lång')
}

### Iterationer

**26** Skapa en ```for-loop``` som skriver ut talen 1 till 100 i konsollen.
for(let i = 1; i <= 100; i++){
  console.log(i)
}

**27** Gör om övning 26, men använd denna gången en ```while-loop```. Vilka justerngar behöver du göra?
let i = 0;

while(i <= 100){
  console.log(i)
  i++
}

**28** Skapa en ```for-loop``` så körs 100 gånger. Inuti varje loop skall du slumpa fram ett tal mellan 1 - 100. Räkna sedan ut medelvärdet av dina 100 slumpningar.
for(let i = 0; i <= 100; i++){
  let randomNum = Math.floor(Math.random() * 100) + 1 / 100
  console.log(randomNum)
}

**29** Skapa en ```while-loop``` som körs tills du lyckats slumpa fram ett valt tal mellan 1 - 100. Levelup: håll koll på hur många gånger du slumpat och skriv sedan ut detta i konsollen.
let myNum = 5
let guesses = 0;

while(true){
  let randomNum = Math.floor(Math.random() * 100) + 1
  guesses++
  if(randomNum === myNum){
    break
  }
}
console.log(`You've had ${guesses} guesses`)

**30** Be användaren mata in sitt födelsedatum enligt (YYYYMMDD-XXXX). Använd en ```while-loop``` som körs tills användaren har angett korrekt antal tecken. Skriv sedan ut användarens fyra sista siffror i konsollen.

let födelseDatum = prompt("Ange födelsedatum i formatet (YYYYMMDD-XXXX)");

```javascript
let correctInput = false;
while() {
  let birthdate = prompt("Ange födelsedatum i formatet (YYYYMMDD-XXXX)");
}
```
