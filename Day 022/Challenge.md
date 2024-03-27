1. Add an `@State` property to store the user’s score, modify it when they get an answer right or wrong, then display it in the alert and in the score label.
2. When someone chooses the wrong flag, tell them their mistake in your alert message – something like “Wrong! That’s the flag of France,” for example.
3. Make the game show only 8 questions, at which point they see a final alert judging their score and can restart the game.

**Note:** That last one takes a little more thinking than the others. A good place to start would be to add a second `alert()` modifier watching a different Boolean property, then connect its button to a `reset()`method to set the game back to its initial state.

Challenge solved in repository -> https://github.com/mkostrzycki/100dos-GuessTheFlag
