# a-b-c-d

a/b + c/d

Problem Description

给你2个分数，求他们的和，并要求和为最简形式。

Input

输入首先包含一个正整数T（T<=1000），表示有T组测试数据，然后是T行数据，每行包含四个正整数a,b,c,d（0<a,b,c,d<1000），表示两个分数a/b 和 c/d。

Output

对于每组测试数据，输出两个整数e和f，表示a/b + c/d的最简化结果是e/f，每组输出占一行。

Sample Input

2 1 2 1 3 4 3 2 3

Sample Output

5 6 2 1


代码：

#include<iostream>
  
using namespace std;

int gcd(int a,int b)

{

    int c=a%b;
    
    while(c)
    
    {
    
        a=b;
        
        b=c;
        
        c=a%b;
        
    }
    
    return b;
    
}

int main()

{

    int n,a,b,c,d,t1,t2,t;
    
    cin>>n;
    
    while(n--)
    
    {
    
        scanf("%d%d%d%d",&a,&b,&c,&d);
        
        t1=a*d+b*c;
        
        t2=b*d;
        
        t=gcd(t1,t2);
        
        printf("%d %d\n",t1/t,t2/t);
        
    }
    
  return 0;
  
}
