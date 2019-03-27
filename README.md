#include<stdio.h>
int main()
{
int n,temp,temp1;
printf("\n enter number of process ");
scanf("%d",&n);
int bt[n];
int at[n];
int p[n];
int wt[n];
int rq[n];

for(int i=0;i<n;i++)
{
	printf("\n Enter Arrival time");
	
    scanf("%d", &at[i]);
	printf("\n Enter Burst time");
	scanf("%d",&bt[i]);
	
}
 //sorting arrival time in ascending order using bubble sort
 for(int i=0;i<n-1;i++)
     {
     	 for(int j=0;j<n-i;j++)
     	 {
     	   if(at[j]>at[j+1])
     	    {
     	    	temp=at[j];
     	    	temp1=bt[j];
     	    	at[j]=at[j+1];
     	    	bt[j]=bt[j+1];
     	    	
     	    	at[j+1]=temp;
     	    	bt[j+1]=temp1;
     	    	
			 }
		  }
	 }
	 printf("\nprocess AT,BT");
    for(int i=0;i<n;i++)
    {
    	printf("\n%d ",at[i]);
    	printf("\n%d " ,bt[i]);
	
	}
}



	
