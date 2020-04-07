# yyh-0607#include<stdio.h>
#include <iostream>
using namespace std;
int i, j, n, a[30];
int Max(int n, int a[]);
int main()
{
    int max1 = 0, flag = 0;
    scanf("%d",&n);
    for (i = 0; i < n; i++)
    {
        scanf("%d",&a[i]);
    }
    for (i = 0; i < n; i++)
    {
        if (a[i] < 0)
        {
                flag = 1;
        }
        flag = 0;
    }
    if (flag == 1)
    {
        printf("0");
    }
    else
    {
        max1 = Max(n, a);
        printf("%d",max1);

    }
}
int Max(int n, int a[])
{
    int x1, x2;
  	x1 = x2 = 0;
  	for (i = 0; i < n; i++)
    {
        x1 = 0;
        for (j = i; j < n; j++)
        {
            x1 += a[j];
            if (x1 > x2)
            {
                x2 = x1;
            }
        }
  	}
  	return x2;
}
