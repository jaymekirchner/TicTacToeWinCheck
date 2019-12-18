# TicTacToeWinCheck
My code to check who won in a tic-tac-toe Java game
    
    
    /**
     * Checks if the game has ended either because a player has won, or if the game has ended as a tie.
     * If game hasn't ended the return string has to be "None",
     * If the game ends as tie, the return string has to be "Tie",
     * If the game ends because there's a winner, it should return "X wins" or "O wins" accordingly
     * @param grid 2D array of characters representing the game board
     * @return String indicating the outcome of the game: "X wins" or "O wins" or "Tie" or "None"
     */
    public String checkGameWinner(char[][] grid){
        String result = "None";
        //Student code goes here ...
        
        if ((grid[0][0] != '-') && (grid[0][0] == 'x' || grid[0][0] == 'o') && (grid[0][0] == grid[1][0]) && (grid[1][0] == grid[2][0])) {
        	result = grid[0][0] + " wins";
        	return result;
        } else if ((grid[0][1] != '-') && (grid[0][1] == grid[1][1]) && (grid[1][1] == grid[2][1])){
        	result = grid[0][1] + " wins";
        	return result;
        } else if ((grid[0][2] != '-') && (grid[0][2] == grid[1][2]) && (grid[1][2] == grid[2][2])) {
        	result = grid[0][2] + " wins";
        	return result;
        } else if ((grid[0][0] != '-') && (grid[0][0] == grid[0][1]) && (grid[0][1] == grid[0][2])) {
        	result = grid[0][0] + " wins";
        	return result;
        } else if ((grid[1][0] != '-') && (grid[1][0] == grid[1][1]) && (grid[1][1] == grid[1][2])) {
        	result = grid[1][0] + " wins";
        	return result;
        } else if ((grid[2][0] != '-') && (grid[2][0] == grid[2][1]) && (grid[2][1] == grid[2][2])) {
        	result = grid[2][0] + " wins";
        	return result;
        } else if ((grid[0][0] != '-') && (grid[0][0] == grid[1][1]) && (grid[1][1] == grid[2][2])) {
        	result = grid[0][0] + " wins";
        	return result;
        } else if ((grid[2][0] != '-') && (grid[2][0] == grid[1][1]) && (grid[1][1] == grid[0][2])) {
        	result = grid[2][0] + " wins";
        	return result;
        } else if ((grid[0][0] != '-') && (grid[1][0] != '-') && (grid[2][0] != '-') 
        		&& (grid[0][1] != '-') && (grid[1][1] != '-') && (grid[2][1] != '-') 
        		&& (grid[0][2] != '-') && (grid[1][2] != '-') && (grid[2][2] != '-')){
        		result = "Tie"; 
        		return result;
        } else {
        	return result;
        }
    }
