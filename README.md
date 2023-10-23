
# RegEx

Recap course RegEx from this link 👉 [freecodecamp](https://www.youtube.com/watch?v=ZfQFUJhPqMM&t=54s)


## Contents
Using Javascript for test

#### Using the Test Method

```javascript
  let myString = "Hello, World!";
  let myRegex = /Hello/;
  let result = myRegex.test(myString); // Return true
```

#### Match Literal Strings

```javascript
  let waldoIsHiding = "Somewhere Waldo is hiding in this text.";
  let waldoRegex = /Waldo/;
  let result = waldoRegex.test(waldoIsHiding); // Return true
```

#### Match a Literal String with Different Possibilities

```javascript
  let petString = "James has a pet cat.";
  let petRegex = /dog|cat|fish|bird/; // Change this line
  let result = petRegex.test(petString);  // Return true
```

#### Ignore Case While Matching

```javascript
  let myString = "freeCodeCamp";
  let fccRegex = /freeCodeCamp/i; // Change this line
  let result = fccRegex.test(myString);   // Return true
```

#### Extract Matches

```javascript
  let extractStr = "Extract the word 'coding' from this string.";
  let codingRegex = /coding/;
  let result = extractStr.match(codingRegex); // Return ['codeing']
```

#### Find More Than the First Match

```javascript
  let twinkleStar = "Twinkle, twinkle, little star";
  let starRegex = /twinkle/gi;
  let result = twinkleStar.match(starRegex); // Return ['Twinkle','twinkle']
```

#### Match Anything with Wildcard Period

```javascript
  let humStr = "I'll hum a song";
  let hugStr = "Bear hug";
  let huRegex = /hu./;
  humStr.match(huRegex);  // Return hum
  hugStr.match(huRegex); // Return hug

  let exampleStr = "Let's have fun with regular expressions!";
  let unRegex = /.un/; // Change this line
  let result = unRegex.test(exampleStr);  // Return true
```

#### Match Single Character with Multiple Possibilities

```javascript
  let bigStr = "big";
  let bagStr = "bag";
  let bugStr = "bug";
  let bogStr = "bog";
  let bgRegex = /b[aiu]g/;
  bigStr.match(bgRegex); // Return big
  bagStr.match(bgRegex); // Return bag
  bugStr.match(bgRegex);  // Return bug
  bogStr.match(bgRegex); // Return null

  let quoteSample =
    "Beware of bugs in the above code; I have only proved it correct, not tried it.";
  let vowelRegex = /[aeiou]/gi; // Change this line
  let result = quoteSample.match(vowelRegex);  
  // Return ['e', 'a', 'e', 'o', 'u', 'i', 'e', 'a', 'o', 'e', 'o', 'e', 'I', 'a', 'e', 'o', 'o', 'e', 'i', 'o', 'e', 'o', 'i', 'e', 'i']
```

#### Match Letters of the Alphabet

```javascript
  let catStr = "cat";
  let batStr = "bat";
  let matStr = "mat";
  let bgRegex = /[a-e]at/;
  catStr.match(bgRegex); // Return cat
  batStr.match(bgRegex); // Return bat
  matStr.match(bgRegex); // Return null

  let quoteSample = "The quick brown fox jumps over the lazy dog.";
  let alphabetRegex = /[a-z]/ig; // Change this line
  let result = quoteSample.match(alphabetRegex); 
  // Return ['T', 'h', 'e', 'q', 'u', 'i', 'c', 'k', 'b', 'r', 'o', 'w', 'n', 'f', 'o', 'x', 'j', 'u', 'm', 'p', 's', 'o', 'v', 'e', 'r', 't', 'h', 'e', 'l', 'a', 'z', 'y', 'd', 'o', 'g']
```

#### Match Numbers and Letters of the Alphabet

```javascript
  let quoteSample = "Blueberry 3.141592653s are delicious.";
  let myRegex = /[h-s2-6]/ig; // Change this line
  let result = quoteSample.match(myRegex); // Change this line
  // Return ['l', 'r', 'r', '3', '4', '5', '2', '6', '5', '3', 's', 'r', 'l', 'i', 'i', 'o', 's']
```

#### Match Single Characters Not Specified

```javascript
  let quoteSample = "3 blind mice.";
  let myRegex = /[^aeiou.!{@}]/gi; // Change this line
  let result = quoteSample.match(myRegex); // Change this line
  // Return ['3', ' ', 'b', 'l', 'n', 'd', ' ', 'm', 'c']
```

#### Match Characters that Occur One or More Times

```javascript
  let difficultSpelling = "Mississippi";
  let myRegex = /s+/g; // Change this line
  let result = difficultSpelling.match(myRegex);
  // Return ['ss', 'ss']
```

#### Match Characters that Occur Zero or More Times

```javascript
  let soccerWord = "gooooooooal!";
  let gPhrase = "gut feeling";
  let oPhrase = "over the moon";
  let goRegex = /go*/;
  soccerWord.match(goRegex); // Return ['goooooooo']
  gPhrase.match(goRegex); // Return ['g']
  oPhrase.match(goRegex); // Return null

  let chewieQuote = "Aaaaaaaaaaaaaaaarrrgh!"; // Change this line
  let chewieRegex = /Aa*/; // Change this line
  let result = chewieQuote.match(chewieRegex);
  // Return ['Aaaaaaaaaaaaaaaa']
```

#### Find Characters with Lazy Matching

```javascript
  let string = "titanic";
  let regex = /t[a-z]*i/;
  string.match(regex); // Return ['titani']

  let text = "<h1>Winter is coming</h1>";
  let myRegex = /<.*>/;
  let result = text.match(myRegex); // Return ['<h1>Winter is coming</h1>']
```

#### Find One or More Criminals in a Hunt

```javascript
  let crowd = 'P1P2P3P4P5P6P7P8P9';
  let reCriminals = /./;

  let matchedCriminals = crowd.match(reCriminals); // Return ['P']
```

#### Match Beginning String Patterns

```javascript
  let rickyAndCal = "Cal and Ricky both like racing";
  let calRegex = /^Cal/;
  let result = calRegex.test(rickyAndCal); // return true
```

#### Match Ending String Patterns

```javascript
  let caboose = "The last car on a train is the caboose";
  let lastRegex = /caboose$/;
  let result = lastRegex.test(caboose); // return true
```

#### Match All Letters and Numbers

```javascript
  let quouteSample = "The five boxing wizards jump quickly";
  let alphabetRegexV2 = /\w/g;
  let result = quouteSample.match(alphabetRegexV2).length; // return 31
```

#### Match Everything But Letters and Numbers

```javascript
  let quouteSample = "The five boxing wizards jump quickly.";
  let alphabetRegexV2 = /\W/g;
  let result = quouteSample.match(alphabetRegexV2).length; // return 6
```

#### Match All Numbers

```javascript
  let numString = "Your sandwich will be $5.00";
  let numRegex = /\d/g;
  let result = numString.match(numRegex).length; // return 3
```

#### Match All Non-Numbers

```javascript
  let numString = "Your sandwich will be $5.00";
  let numRegex = /\D/g;
  let result = numString.match(numRegex).length; // return 24
```

#### Restrict Possible Usernames

```javascript
  let username = "JackOfAllTrades";
  let userCheck = /^[A-za-z]{2,}\d*$/;
  let result = userCheck.test(username); // return true
```

#### Match Whitespace

```javascript
  let sample = "Whitespace is important in separating words";
  let countWhiteSpace = /\s/g;
  let result = sample.match(countWhiteSpace); 
  // return [' ', ' ', ' ', ' ', ' ']
```

#### Match Non-White-space Characters

```javascript
  let sample = "Whitespace is important in separating words";
  let countWhiteSpace = /\S/g;
  let result = sample.match(countWhiteSpace);
  // retrun ['W', 'h', 'i', 't', 'e', 's', 'p', 'a', 'c', 'e', 'i', 's', 'i', 'm', 'p', 'o', 'r', 't', 'a', 'n', 't', 'i', 'n', 's', 'e', 'p', 'a', 'r', 'a', 't', 'i', 'n', 'g', 'w', 'o', 'r', 'd', 's']
```

#### Specify Upper and Lower Number of Matches

```javascript
  
```

#### Specify Only the Lower Number of Matches

```javascript
  
```

#### Specify Exact Number of Matches

```javascript
  
```

#### Check for All or None

```javascript
  
```

#### Positive and Negative Lookahead

```javascript
  
```

#### Reuse Patterns Using Capture Groups

```javascript
  
```

#### Use Capture Groups to Search and Replace

```javascript
  
```

#### Remove Whitespace from Start and End

```javascript
  
```
