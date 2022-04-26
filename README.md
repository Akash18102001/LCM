#include<stdio.h>
int LCM(int,int); 			//Function prototype declaration 

int main()
{
	int a, i, j;
	printf(" Enter any two number whose LCM to be calculated : ");
	scanf("%d%d",&i,&j);    //Scanning & storing input
	a = LCM(i,j);			//function call
	printf("\n The LCM of %d and %d is %d",i,j,a);//prints the result
	return 0;
	
}

int LCM(int m,int n)  		//Recursive function definition 
{
	static int k=1;			//static variable is initialized only once for each function call
	if((k % m == 0 ) && ( k % n == 0 ))
	{
		return k;
	}
	else
	{
		k++;
		LCM(m,n);
		return k;
	}
}
