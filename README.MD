# CHANGES MADE

### replaced these lines

statusDisplay.textContent = messages.gameWon;
statusDisplay.textContent = messages.gameDraw;
statusDisplay.textContent = messages.playerTurn;


### with

statusDisplay.textContent = messages.gameWon();
statusDisplay.textContent = messages.gameDraw();
statusDisplay.textContent = messages.playerTurn();
as they are all function calls


### replaced this inside the handleRestartGame()

cells.forEach(cell => {
    cell.textContent = '';
});

### with

cells.forEach(cell => {
    cell.textContent = '';
    cell.classList.remove('winner');
});
as the previous one didnt remove the winner highlight.

### added this

restartButton.addEventListener('click', handleRestartGame);
as the restart button had no functionality.