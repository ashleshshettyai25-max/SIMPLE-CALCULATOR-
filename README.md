
#include<stdio.h>
#include<math.h>


void print_menu();

int main()
{
int choice;
double first,second,result;

while(1){
print_menu();
scanf("%d",&choice);

if(choice==9)
{
break;
}

if(choice<1 || choice>9)
{
fprintf(stderr,"invalid menu choice");
continue;
}

printf("\nPLEASE ENTER THE FIRST NUMBER:");
scanf("%lf",&first);
printf("NOW ENTER THE SECOND NUMBER:");
scanf("%lf",&second);

switch(choice)
{
case 1://ADD
result=first+second;
break;

case 2://SUBTRACT
result=first-second;
break;

case 3://MULTIPLY
result=first*second;
break;

case 4://DIVIDE
if(second!=0){
result=first/second;}
else
{ result=NAN;
printf("MATH ERROR");

}
break;

case 5://MODULUS
if(second!=0){
result=(int)first%(int)second;}
else{ result=NAN;
printf("MATH ERROR");

}
break;

case 6://POWER
result=pow(first,second);
break;

case 7://sqaureroot
result=pow(first,0.5);
break;

case 8://cuberoot
result=pow(first,0.3333333333333333);
break;
}

if(isnan(result))
{
continue;

}
else{
printf("\nRESULT OF THE OPERATION IS %.2f\n",result);
}


}
return 0;

}
void print_menu()
{
printf("\n---------WELCOME TO SIMPLE CALCULATOR---------\n");
printf("\nchoose one of the following operation");
printf("\n1.ADDITION");
printf("\n2.SUBTRACTION");
printf("\n3.MULTIPLICATION");
printf("\n4.DIVISION");
printf("\n5.MODULUS");
printf("\n6.POWER");
printf("\n7.SQUARE_ROOT");
printf("\n8.CUBE_ROOT");
printf("\n9.EXIT");

printf("\nENTER YOUR CHOICE:");
}
