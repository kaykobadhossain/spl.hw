#include<stdio.h>
#include<string.h>
#include<conio.h>
#include<ctype.h>
#include<math.h>
struct player
   {
      char name[50];
      int run[5];
    };


int main()
{
    struct player player1,player2;
    scanf("%s",player1.name);
    int i;
    double sum = 0,temp=0;
    for(i=0;i<5;i++){
        scanf("%d",&player1.run[i]);
        sum = sum + player1.run[i];
    }
    sum = sum/5;
    for(i=0;i<5;i++){
        temp = temp + (sum-player1.run[i])*(sum-player1.run[i]);
    }
    temp = sqrt(temp/2);
    scanf("%s",player2.name);

    double temp2=0;


      for(i=0;i<5;i++){
        scanf("%d",&player2.run[i]);
        sum = sum + player2.run[i];
    }
    sum = sum/5;
    for(i=0;i<5;i++){
        temp2 = temp2 + (sum-player2.run[i])*(sum-player2.run[i]);
    }
    temp2 = sqrt(temp2/2);
    if(temp>temp2){
        printf("More consistant player is %s",player2.name,temp2,temp);
    }
    else if(temp<temp2){
        printf("More consistant player is %s",player1.name,temp,temp2);
    }
    else{
        printf("Both are equally consistant");
    }

    return 0;
}
