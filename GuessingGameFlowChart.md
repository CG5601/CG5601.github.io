```mermaid
flowchart TD
    Start([Start]) --> GenerateRandomNumber[("Generate Random Number between 1 and 100")]
    GenerateRandomNumber --> InputGuess[("Input Guess (1-100)")]
    InputGuess --> ValidateInput{Is the guess a number between 1 and 100?}
    ValidateInput -->|No| Invalid[("Print 'Invalid Number or Input' and prompt again")]
    ValidateInput -->|Yes| CheckGuess[("Check Guess")]
    CheckGuess -->|Too High| TooHigh[("Print 'Too High' and prompt again")]
    CheckGuess -->|Too Low| TooLow[("Print 'Too Low' and prompt again")]
    CheckGuess -->|Correct| CorrectGuess[("Print 'You are Correct!' and end game")]
    TooHigh --> InputGuess
    TooLow --> InputGuess
    InvalidInput --> InputGuess
    CorrectGuess --> End([End])
```

When you first start up the random number generator it will ask for you to input a guess between numbers 1-100. It will check if the number you input is within the correct range. If you insert an invalid value it will give you an error and tell you to input a proper value. If you input a proper value it will tell you if you are too high or too low from the correct number. When you input the correct guess the game will prompt you with a congrats and end the game.