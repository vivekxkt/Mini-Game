#include <stdio.h>
#include <stdlib.h>
#include<time.h>

int main()
{
    int number1;
    int ui;

    printf("Your turn\n");
    printf("[0 : Stone , 1 : Paper , 2 : scisor\n");
    
    printf("Enter any number from 0 to 2 :");
    scanf("%d",&ui);

    if (ui==0){
        printf("Your choice : Stone \n"); 
    }
    else if(ui==1){
        printf("Your choice : Paper \n");

    }
    else{
        printf("Your choice : Scisor \n");
    }

    
    srand(time(NULL));
    number1= rand() % 3;


    if (number1==ui){
        printf("Its a Draw :|");
    }

    else if (number1==0 && ui==1){
        printf("You Won :) \n");
        printf("CPU's Choice : Stone\n");

        
    }
    else if (number1==0 && ui==2){
        printf("you lost :(\n");
        printf("CPU's Choice : Stone\n");


    }
    else if (number1==1 && ui==0){
        printf("You lost :)\n");
        printf("CPU's Choice : Paper\n");

        
    }
    else if (number1==1 && ui==2){
        printf("you won :(\n");
        printf("CPU's Choice : Paper\n");

    }
    else if (number1==2 && ui==0){
        printf("You Won :)\n");
        printf("CPU's Choice : Scisor\n");
        
    }
    else if (number1==2 && ui==1){
        printf("you lost :(\n");
        printf("CPU's Choice : Scisor\n");

    }
    printf("Game over");

    return 0;

}
