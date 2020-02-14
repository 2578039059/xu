#include "stdio.h"
#include<string.h>
#include<math.h>
	char dx(int n)
	{
   	 if(n==0) printf("零");
   	 if(n==1) printf("一");
    	if(n==2) printf("二");
   	 if(n==3) printf("三");
	    if(n==4) printf("四");
   	 if(n==5) printf("五");
   	 if(n==6) printf("六");
   	 if(n==7) printf("七");
   	 if(n==8) printf("八");
    	if(n==9) printf("九");
	}
int change(char s[])
{
    if(strcmp(s,"一")==0) 
        return 1;
    if(strcmp(s,"二")==0) 
        return 2;
    if(strcmp(s,"三")==0) 
        return 3;
    if(strcmp(s,"四")==0) 
        return 4;
    if(strcmp(s,"五")==0) 
        return 5;
    if(strcmp(s,"六")==0) 
        return 6;
    if(strcmp(s,"七")==0) 
        return 7;
    if(strcmp(s,"八")==0) 
        return 8;
    if(strcmp(s,"九")==0) 
        return 9;
    if(strcmp(s,"零")==0) 
        return 0;
	if(strcmp(s,"十")==0) 
        return 10;
    
}
int main()
{
	
	int sum=0;
	char a[20],b[20],c[20],d[20],ad[20],l[20],x[20],fir[20],num[20];
	char q[20],w[20],e[20],r[20],t[20],y[20],u[20],i[20],o[20];
	scanf("%s %s %s %s",a,b,c,d);
	if(strcmp(c,"等于")==0)
		sum=change(d);
	//printf("%d",sum);
	while((scanf("%s",fir))!=EOF)
	{
		
		if(strcmp(fir,b)==0)
		{
			scanf("%s",ad);
			if(strcmp(ad,"增加")==0)
			{
				scanf("%s",num);
				sum=sum+change(num);
			}
			if(strcmp(ad,"减少")==0)
			{
			scanf("%s",num);
			sum=sum-change(num);
			}
		}
		
		if(strcmp(fir,"看看")==0)
		{
			scanf("%s",l);
			//printf("%s",dx(sum));
				
		}
		if(strcmp(fir,"如果")==0)
		{
			scanf("%s %s %s %s %s %s %s %s %s",q,w,e,r,t,y,u,i,o);
			if(sum >= change(r))
			{dx(sum);printf("\n%s",y);}
			else
			{printf("%s",o);}
		}

	}
}
