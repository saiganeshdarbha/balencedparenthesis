# balencedparenthesis
#include <stdio.h>
int stack[50],top=-1;
void push(int t)
{            
       top=top+1;
       stack[top]=t;
}
int pop()
{
   int te=stack[top];
   top=top-1;
   return te;
}
main()
{
   int a[50],n=4,i,temp;
   for(i=0;i<n;i++)
          scanf("%d",&a[i]);
   for(i=0;i<n;i++)
   {
         if(a[i] > 0)
              push(a[i]);
         else
        {
                if(top == -1)
               {
                      printf("invalid expression");
                      exit(0);
               }
               temp = pop();
               else
              {
                      if(temp !=(-a[i]))
                    {
                             printf("invalid expression");
                             exit(0);
                     }
              }
         }
   }
   if(top >=0 )
        printf("invalid");
   else
        printf("valid");
}
