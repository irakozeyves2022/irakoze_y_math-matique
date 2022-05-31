EQUATION DU SECOND DEGRE(POGRAMMATION EN PARALLELE)


  SOLUTION
  

#include<stdio.h>
#include<math.h>
int main()
{
       float a,b,c,D,x,y,d;
       printf("\n\n\tce programme permet de resoudre les equations de second degre\n");
       printf("\n\n\tSaisir A = ");
       scanf("%f",&a);
       printf("\n\n\tSaisir B = ");
       scanf("%f",&b);
       printf("\n\n\tSaisir C = ");
       scanf("%f",&c);       
 D=(b*b)-(4*a*c);
       if(a==0 ){
            if( b!=0 ){
               x=-c/b;
               printf("\n\n\tLa Solution est : x = %.2f",x);
            }else if( c==0 ){
               printf("\n\n\t\tSolution quelconq"); 
            }else{
               system("color fc");
               printf("\n\n\t\tSolution impssible !\n\t\t %.2f != 0",c);
            }
       }else if( D==0 ){
               x=-b/(2*a);
               printf ("\n Delta = (%.2f)^2 - 4(%.2f)(%.2f) = %.2f\n\n Donc",b,a,c,D);
               printf ("\n\n L'equation admet une solution : \n\n\t\tx = -b/2a \n\n\t\t  = %.2f",x);
       }else if( D!=0 ){
               if( D>0 ){
                 d=sqrt(D); 
                 x=(d-b)/(2*a);
                 y=(-d-b)/(2*a);
                 printf ("\n Le discriminant D = (%.2f)^2 - 4(%.2f)(%.2f) = %.2f > 0",b,a,c,D);
                 printf ("\n Soit d = %.2f , la Racine carre de D\n\n Donc",d); 
                 printf ("\n\n L'equation admet deux solutions x & x'"); 
                 printf ("\n\n\tx = d-b/2a \t\t\t x'= -d-b/2a");
                 printf ("\n\n\tx = %.2f     \t\t x' = %.2f",x,y);
               }else{
                 d=sqrt(-D);
                 printf("\n\n Le discriminant D = %.2f < 0",D);
                 printf("\n L equation n'admet pas de solution dans R\n\n");
                 printf("La solution dans C :\n  Soit d = (%.2f)i ,& d^2 = -D",d);
                 x=b/(2*a);
                 y=d/(2*a);
                 printf("\n\n\t z  =  d-b/2a\t =  (%.2f)i - %.2f",y,x);
                 printf("\n\n\t z' = -d-b/2a\t = -(%.2f)i - %.2f",y,x);
               } 
       }
       getch();
       return 0;
}
