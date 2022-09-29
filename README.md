#include <stdio.h> 
#include <stdlib.h> 
#include <stdbool.h> 
#include <math.h> 
#include <string.h>

/* int board[25] = { :,:,:,:,:, :,O,-,X,:, :,X,-,-,:, :,-,-,-,:, :,:,:,:,:, } 
*/ // Create the constants for the board pieces 
const NOUGHTS = 1; 
const CROSSES = 2; 
const BORDER = 8; 
const EMPTY = 0;

int* ptr1, * ptr2; ptr1 = NOUGHTS; ptr2 = CROSSES;

const int ConvertTo25[9] = { 6,7,8, 11,12,13,16,17,18}; 
//Base board design // Creating the board struct struct TTT_BoardGame { unsigned short playerTurn; int boardSqrt; double boardLen; bool canFinish; char board[3][3][3]; };

// Initializing the board struct struct TTT_BoardGame ttt_init(void) { struct TTT_BoardGame game = { 0 }; game.playerTurn = 0; game.boardSqrt = 3; game.boardLen = game.boardSqrt * game.boardSqrt; game.canFinish = false;

// Set the starting value in each board cell
char pos[3] = { '0', '0', '1' };
for (unsigned short v = 0; v < game.boardSqrt; v++) {
	for (unsigned short h = 0; h < game.boardSqrt; h++) {
		for (short p = 2; p >= 0; p--) {
			game.board[v][h][p] = pos[p];
		}
		if (pos[2] < '9')
			pos[2]++;
		else {
			pos[2] = '0';
			pos[1]++;
		}

		if (pos[1] > '9') {
			pos[1] = '0';
			pos[0]++;
		}
	}
}
return game;
} //Initial welcome information and the board print design void PrintBoard(const int* board) { int index = 0; printf("\nWelcome to my Tic-Tac-Toe Game\nBy: Mark Plucinski\n\n\nBoard:\n"); for (index = 0; index < 25; ++index) { if (index != 0 && index % 5 == 0) printf("\n"); } printf("%4d", board[index]); }

{ // constants const char s[3] = { '*', 'X', 'O' }; }

//Contains the area where you can add "board[ConvertTo25[0]] =" with the addition of "CROSSES;" or "Nought;" for X or O int main(); { int board[25]; InitialiseBoard(&board[0]); board[ConvertTo25[0]] = CROSSES; board[ConvertTo25[5]] = NOUGHTS; PrintBoard(&board[0]);

return 0;
}
