
<!-- Header -->
# Welcome to Guess the Number Game! 🎮

Can you guess the number I'm thinking of? Give it a try!

<!-- Game Section -->
## Guess the Number:

```html
<script>
  // Generate a random number between 1 and 100
  const secretNumber = Math.floor(Math.random() * 100) + 1;

  function guessNumber() {
    // Get the user's guess
    const userGuess = parseInt(prompt("Enter your guess (between 1 and 100):"));

    // Check if the guess is correct, too high, or too low
    if (userGuess === secretNumber) {
      alert("Congratulations! You guessed the correct number!");
    } else if (userGuess < secretNumber) {
      alert("Too low! Try again.");
      guessNumber(); // Recursive call to keep guessing
    } else {
      alert("Too high! Try again.");
      guessNumber(); // Recursive call to keep guessing
    }
  }

  // Start the game
  guessNumber();
</script>
