# Binary-addition

#include <stdio.h>

int main()
{

    printf("Hello World");
    int n1,n2,rem=0,c[100],a,b,i=1,j;
    scanf("%d",&n1);
    
      scanf("%d",&a);
       scanf("%d",&b);
    
    while (a != 0 || b != 0)
    {
            if(a%10+b%10+rem==2)
            {
                c[i]=0;
                rem=1;
                i++;
                a=a/10;
                b=b/10;
            }
            else if(a%10+b%10+rem==1)
            {
                c[i]=1;
                rem=0;
                i++;
                a=a/10;
                b=b/10;
            }
            else if(a%10+b%10+rem==3)
            {
                c[i]=1;
                rem=1;
                i++;
                a=a/10;
                b=b/10;
            }
            else
            {
                c[i]=0;
                rem=0;
                i++;
                a=a/10;
                b=b/10;
            }
            
        
    }
    c[0]=rem;
    int n=i;
    for(int i=0;i<n;i++)
      printf("%d",c[i]);
    return 0;

}
