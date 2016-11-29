#include<stdio.h>  
int main()  
{  
    int num = 0;               
    int count = 0;               
    int i = 0;  
    printf("请输入一个十进制数：\n");               
    scanf("%d",&num);  
    printf("它的二进制数：\n");                
    for (i=31; i>=0; i--)                  
    {                                       
        printf("%d",(num>>i)&1);          
    }                                         
    printf("\n");                            
                                             
    printf("它的二进制数中1的个数：\n");  
    while (num)  
    {  
        count++;   //由于第一次已经进入循环，因此需要提前加1  
        num = num&(num-1);   
    }  
    printf("%d\n",count); //输出1的个数 
    return 0;  
}  
