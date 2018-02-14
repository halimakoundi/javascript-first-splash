# A first splash into JavaScript

This is taking the tutorial provided by Mozilla [MDN Web Doc](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/A_first_splash) and breaking down the main function `checkGuess()` .

## Storing information

```javascript
  var userGuess = Number(guessField.value);
```

This declares a variable called userGuess and sets its value to the current value entered inside the text field. We also run this value through the built-in Number() method, just to make sure the value is definitely a number.

* Now the function looks like this:
```javascript
function checkGuess() {
  var userGuess = Number(guessField.value);
}
```

## Branching (or Conditional)

```javascript
  if (guessCount === 1) {
    guesses.textContent = 'Previous guesses: ';
  }
```

Next, we encounter our first conditional code block.
A conditional code block allows you to run code selectively, depending on whether a certain condition is true or not. It looks a bit like a function, but it isn't. The simplest form of conditional block starts with the keyword if, then some parentheses, then some curly braces. Inside the parentheses we include a test. If the test returns true, we run the code inside the curly braces. If not, we don't, and move on to the next bit of code. In this case the test is testing whether the guessCount variable is equal to 1 (i.e. whether this is the player's first go or not).
If it is, we make the guesses paragraph's text content equal to "Previous guesses: ". If not, we don't.

* Now the function looks like this:
```javascript
function checkGuess() {
  var userGuess = Number(guessField.value);
  if (guessCount === 1) {
    guesses.textContent = 'Previous guesses: ';
  }
}
```

## String Manipulation

```javascript
  guesses.textContent += userGuess + ' ';
```

This appends the current `userGuess` value onto the end of the guesses paragraph, plus a blank space so there will be a space between each guess shown.

* Now the function looks like this:
```javascript
function checkGuess() {
  var userGuess = Number(guessField.value);
  if (guessCount === 1) {
    guesses.textContent = 'Previous guesses: ';
  }
  guesses.textContent += userGuess + ' ';
}
```
