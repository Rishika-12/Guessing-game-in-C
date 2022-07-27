# Guessing-game-in-C
#include<stdio.h>
#include<time.h>
#include<stdlib.h>
int main(){
    const int MIN=1;
    const int MAX=100;
    int guess;
    int gusses;
    int ans;
    //use current time as seed
    srand(time(0));
    //generates random num
    ans=(rand()%MAX)+MIN;
    //printf("%d",ans);
    do{
        printf("Enter a guess between 1 and 100:");
        scanf("%d",&guess);
        if(guess>ans){printf("Too HIGH\n");}
        else if(guess<ans){printf("Too LOW\n");}
        else{printf("Correct ans\n");}
        gusses++;
    }while(guess!=ans);
    printf("*******\n");
    printf("%d\n",ans);
    printf("%d",guess);
}
