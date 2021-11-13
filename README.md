# punteros
#include<stdio.h>
#include<conio.h>
#include<cstdlib>
void suma(float *n1,float*n2);
void resta(float *n1,float *n2);
void multiplicacion(float *n1, float *n2);
void division(float *n1, float *n2);

//FUNCIONES PUNTEROS
void suma(float *n1,float *n2)
{
   float suma;
   suma=*n1+*n2;
   printf("\nEl resultado de la suma es:%2.2f",suma);
}
void resta(float *n1,float *n2)
{
   float resta;
   resta=*n1-*n2;
   printf("\nEl resultado de la resta es: %2.2f",resta);
}
void multiplicacion(float *n1, float *n2)
{
   float multiplicacion;
   multiplicacion=*n1 * *n2;
   printf("\nEl resultado de la multiplicacion es: %2.2f ",multiplicacion);
}
void division(float *n1, float *n2)
{
   float division;
   if(*n2==0){
   printf("\nOPERACION NO VALIDA\n");
   }
   else
   {
   division= *n1/ *n2;
   printf("\nEl resultado de la division es: %2.2f",division);
   }
}
//PRINCIPAL
int main()
{
   int opcion;
 do
 {
   int opc;
   float num1,num2;
   printf("DAME EL PRIMER NUMERO: ");
   scanf("%f",&num1);
   printf("DAME EL SEGUNDO NUMERO: ");
   scanf("%f",&num2);   
   printf("\n\t\tElige una opcion\n");
   printf("1.- SUMA \n");
   printf("2.- RESTA \n");
   printf("3.- MULTIPLICACION \n");
   printf("4.- DIVISION \n");
   scanf("%d",&opc);
   switch(opc)
   {
   case 1: 
      suma(&num1,&num2);
   break;
   case 2:
      resta(&num1,&num2);
   break;
   case 3:
      multiplicacion(&num1,&num2);
   break;
   case 4:
      division(&num1,&num2);
   break;
   }
    printf("\n \nDeseas repetir el programa 1.- SI  2.-NO \n");
    scanf("%d",&opcion);
    system ("cls");
}while(opcion==1);
   return 0;
}
