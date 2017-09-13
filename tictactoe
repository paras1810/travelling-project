

//                     +++++*****GAME-TIC TAC TOE*****+++++
//                               ----------------
//                                         made by-PARAS JAIN && RISHABH JAIN
//                                         ----------------------------------
//                          *****HEADER FILES*****
#include<iostream.h>
#include<conio.h>
#include<stdio.h>
#include<stdlib.h>
//                          *****TIC TAC TOE MATRIX*****
char matrix[3][3];
int a=0;
//                          *****FUNCTION USED*****
char check(void);
void init_matrix();
void get_computer_move();
void get_player_move();
void get_1player_move();
void get_2player_move();
void disp_matrix();
//                          *****MAIN FUNCTION*****
void main()
{clrscr();
char done;
int n;
printf("          *****THIS IS THE GAME OF TIC TAC TOE*****\n");
printf("                                 made by-RISHABH JAIN\n");
printf("                                         PARAS JAIN");
printf("\n\n\n\n                    *****ENTER YOUR CHOICE*****\n\n\n\n");
printf("\n        *****1.IF YOU WANT TO PLAY AGAINST THE COMPUTER*****");
printf("\n        *****2.WHETHER YOU PLAY WITH YOUR OPPOSITION*****\n");
scanf("%d",&n);
done=' ';
init_matrix();
if(n==1)
{
do
{
disp_matrix();
get_computer_move();
done=check();
if(done!=' ')break;
get_player_move();
done=check();
}while(done==' ');
if(done=='X')
printf("PLAYER WON!\n");
else
printf("COMPUTER WON!\n");
disp_matrix();
}
else if(n==2)
{
do
{a=a+2;
disp_matrix();
get_1player_move();
done=check();
if(done!=' ')break;
get_2player_move();
done=check();
}while(done==' '&&a<8);
if(done=='2')
printf("PLAYER 2 WON!\n");
else if(done=='1')
printf("PLAYER 1 WON!\n");
else
printf("MATCH DRAW\n");
disp_matrix();
}
else
{
printf("!!!!!WRONG CHOICE!!!!!\n");
exit(0);
}
getch();
}
//                          *****INITIALIZE THE MATRIX*****
void init_matrix()
{
int i,j;
for(i=0;i<3;i++)
for(j=0;j<3;j++)
matrix[i][j]=' ';
}
//                          *****GET A PLAYER MOVE*****
void get_player_move()
{
int x,y;
printf("ENTER X,Y COORDINATE FOR YOUR MOVE:");
scanf("%d%*c%d",&x,&y);
x--;y--;
if(matrix[x][y]!=' ')
{
printf("INVALID MOVE,TRY AGAIN\n");
get_player_move();
}
else matrix[x][y]='X';
}
void get_1player_move()
{
int x,y;
printf("ENTER X,Y COORDINATE FOR YOUR MOVE:");
scanf("%d%*c%d",&x,&y);
x--;y--;
if(matrix[x][y]!=' ')
{
printf("INVALID MOVE,TRY AGAIN\n");
get_1player_move();
}
else matrix[x][y]='1';
}
void get_2player_move()
{
int x,y;
printf("ENTER X,Y COORDINATE FOR YOUR MOVE:");
scanf("%d%*c%d",&x,&y);
x--;y--;
if(matrix[x][y]!=' ')
{
printf("INVALID MOVE,TRY AGAIN\n");
get_2player_move();
}
else matrix[x][y]='2';
}
//                         *****GET THE COMPUTER MOVE*****
void get_computer_move()
{
int i,j;
for(i=0;i<3;i++)
{
for(j=0;j<3;j++)
if(matrix[i][j]==' ')break;
if(matrix[i][j]==' ')break;
}
if(i*j==9)
{
printf("draw\n");
exit(0);
}
else
matrix[i][j]='0';
}
//                          *****DISPLAY THE MATRIX*****
void disp_matrix()
{
int t;
for(t=0;t<3;t++)
{
printf("  %c|  %c|  %c",matrix[t][0],matrix[t][1],matrix[t][2]);
if(t!=2)printf("\n---|---|---\n");
}
printf("\n");
}
//                          *****CHECK THE WINNER*****
char check(void)
{
int i;
for(i=0;i<3;i++)
if(matrix[i][0]==matrix[i][1]&&matrix[i][0]==matrix[i][2])return matrix[i][0];
for(i=0;i<3;i++)
if(matrix[0][i]==matrix[1][i]&&matrix[0][i]==matrix[2][i])return matrix[0][i];
if(matrix[0][0]==matrix[1][1]&&matrix[1][1]==matrix[2][2])return matrix[0][0];
if(matrix[0][2]==matrix[1][1]&&matrix[1][1]==matrix[2][0])return matrix[0][2];
return ' ';
}
//                                                                     end...
