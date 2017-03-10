#include <stdio.h>

int function (int t) /* t = total number of participant */
 {
   int x; /* x = number of my desk */


           for(x=0 ; x<=t ; x++)
            {
             if (2 * x * x == t * t + t)
              {
                  printf ("Found! -- # of participant : %d , # of my desk : %d\n" ,t , x );
              }else
                  ;
            }
             if (t != 2)
               {
                  return function (t-1);
               }else
                 printf("Search is complete!\n\n");
                  return 0;
 }

int main(void)
{
  int n;
  char exit;

    do{
    printf("Enter upper bound:\n");
    scanf("%d" , &n);

    printf("-------------------------------------------------------\n");
    function(n);

    printf("Press '0' to exit!\n");
    scanf(" %c" , &exit);
      }while (exit != '0');

  return 0;
}
