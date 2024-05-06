#include<stdlib.h>
#include<stdio.h>
using namespace std;

int main()
{
	int opcion;
	int r1,r2,r3,r11,r22,r33;
	int v;
	int tipo;
	do {
        
	printf("Menu\n");
	printf("1. Ingresar Resistencias\n");
	printf("2. Ingresar Voltaje\n");
	printf("3. Calcular\n");
	printf("4. SALIR\n");
	printf("Elija una operacion: \n");
	scanf("%d",&opcion);
 
                	                 
	switch(opcion)
	{
		case 1:
             
            printf("Que tipo de circuito es?\n 1)R en Paralelo\n 2)R en Serie\n");
            scanf("%d",&tipo);
           switch(tipo)
	{      
           case 2:
                tipo=tipo;
                printf ("Digite el valor de R1: ");
                scanf ("%d", &r1);
                printf ("Digite el valor de R2: ");
                scanf ("%d", &r2);
                printf("Digite el valor de R3: ");
                scanf ("%d", &r3);
                break;
           case 1:
                tipo=tipo;
                printf ("Digite el valor de R11: ");
                scanf ("%d", &r11);
                printf ("Digite el valor de R22: ");
                scanf ("%d", &r22);
                printf("Digite el valor de R33: ");
                scanf ("%d", &r33);
                break;
           default:
                   printf("incorrecto");
                }
                
            break;
		case 2:
             
			printf ("Digite el Voltaje de la fuente ");
                scanf("%d", &v);
			break;
		case 3:
             int RTSerie;
             float RTParaleloA;
             float RTParaleloB;
             float I,I2;
             RTSerie= r1+r2+r3;
             if(tipo==2){
             //usamos RTSerie..
    			printf("suma Rs: %d\n",RTSerie);
    			printf("Voltaje Fuente %d\n",v);
    			printf("I:%f \n",I);
    			I= (float)v/(float)RTSerie;
    			   printf("Por lo tanto la Intesidad del circuito con resistencias en serie es: %f \n",I);
               }else{
               //Usamos RTParalelo..
    			
                RTParaleloA=(1/(float)r11)+(1/(float)r22)+(1/(float)r33);
                RTParaleloB=(float)1/(float)RTParaleloA;
    			printf("RTotal Paralelo %f",RTParaleloB);
    			I2= (float)v/ RTParaleloB;
    			printf("I:%f \n",I2);
                             printf("Por lo tanto la Intesidad del circuito con resistencias en paralelo es: %f \n",I2);
                             }
            
            
            
		  break;
		  case 4:
               break;
		default: 
			printf("Opcion no valida\n");		
	}
	}
    while(opcion!=4);
	system("pause");
	return 0;
}
