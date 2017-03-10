# include <stdio.h>
# include <math.h>


void midpoint_rule(float a,float b, int n)
{
	double delta_x=((b-a) / n) , mid_x=(a + delta_x / 2) ,  result_1=0 , result_2=0 , function_1 , function_2;


	while(mid_x<b)
	{
	function_1=pow(M_E , (mid_x * mid_x));              /*             function_1 = e ^ (x ^ 2) , function_2 = 2 * (e ^ x) - 2 * x                  */
	function_2=(2 * pow(M_E , mid_x) - 2 * mid_x);

	result_1+=delta_x * function_1;
	result_2+=delta_x * function_2;                       /*           mid_x = (x*)       */
	mid_x+=delta_x;
	}
	printf("Midpoint result for function1: %lf\n" , result_1);
	printf("Midpoint result for function2: %lf\n" , result_2);
	return ;
}

void trapezoid_rule(float a,float b, int n)
{
	double delta_x=((b-a) / n) , result_1=0 , result_2=0 , function_1_1 , function_2_1 , function_1_2 , function_2_2;


	while(a<b)
	{
	function_1_1=pow(M_E , (a * a));
	function_2_1=(2 * pow(M_E , a) - 2 * a);
	a+=delta_x;

	function_1_2=pow(M_E , (a * a));
	function_2_2=(2 * pow(M_E , a) - 2 * a);

	result_1+=(delta_x / 2) * (function_1_1 + function_1_2);
	result_2+=(delta_x / 2) * (function_2_1 + function_2_2);
	}
	printf("Trapezoid result for function1: %lf\n" , result_1);
	printf("Trapezoid result for function2: %lf\n" , result_2);
	return ;
}

void simpsons_rule(float a, float b, int n)
{
	double delta_x=((b-a) / n) , result_1=0 , result_2=0 , function_1_1 , function_2_1 , function_1_2 , function_2_2, function_1_3 , function_2_3;


	while(a<b)
	{
	function_1_1=pow(M_E , (a * a));
	function_2_1=(2 * pow(M_E , a) - 2 * a);
	a+=delta_x;

	function_1_2=pow(M_E , (a * a));
	function_2_2=(2 * pow(M_E , a) - 2 * a);
	a+=delta_x;

	function_1_3=pow(M_E , (a * a));
	function_2_3=(2 * pow(M_E , a) - 2 * a);

	result_1+=(delta_x / 3) * (function_1_1 + 4 * function_1_2 + function_1_3);
	result_2+=(delta_x / 3) * (function_2_1 + 4 * function_2_2 + function_2_3);
	}
	printf("Simpson's result for function1: %lf\n" , result_1);
	printf("Simpson's result for function2: %lf\n" , result_2);
	return ;

}


int main (void)
{
   float a, b;
   int n;
   char exit;

   do{
   printf("Please enter upper limit.\n");
   scanf("%f" , &b);
   printf("Please enter lower limit.\n");
   scanf("%f" , &a);
   printf("Please enter interval count.\n");
   scanf("%d" , &n);
   printf("---------------------------------------------------------------------------\n");
   printf("LB:%f UB: %f INTERVAL: %d\n" , a ,b, n);
   midpoint_rule(a,b,n);
   trapezoid_rule(a,b,n);
   if (n % 2 == 0)
    {simpsons_rule(a,b,n);
    }
   else
     printf("n must be even for Simpson's rule!!\n");
   printf("Press '0' to exit!\n");
   scanf(" %c", &exit);
   }while(exit != '0');

return 0;
}
