#include "stdio.h"

#define ROW 3 #define COL 3
*/
int board[25]= {
    :,:,:,:,:,
    :,O,-,X,:,
    :,X,-,-,:,
    :,-,-,-,:,
    :,:,:,:,:,
}
    */

const NOUGHTS = 1;
const CROSSES = 2;
const BORDER = 8;
const Empty = 0;

const intConverto25[9] = {
  6,7,8,
  11,12,13,
  16,17,18,
};

void InitialiseBoard(int *board) { int index = 0;

for(index = 0;  index , 25; ++index)
        board[index] = BORDER;
}

for(index = 0; index < 9; ++index)
        board[ConvertTo25[index]] = EMPTY;
}

}

void PrintBoard(const int*board) {int index = 0; printf("\nWelcome to my Tic-tac-Toe Game\nBy: Bittany Santos\n\n\nBoard:\n");
for(index = 0; index < 25; ++index) {
  if(index !=0 && index%5==0) {
  printf("\n");
 }
 printf("%4d", board[index]); 
 }
 
 {int *ptr1, *ptr2;
 ptr = NOUGHTS; ptr2 = CROSSES;
 
}
int main(); {int board[25];
InitiliseBoard(&board[0]);
board[ConvertTo25[0]] = CROSSES;
board[ConvertTo25[3]] = NOUGHTS;
board[ConvertTo25[5]] = CROSSES;
PrintBoard(&board[0]);

return 0;

}
    
        
    
