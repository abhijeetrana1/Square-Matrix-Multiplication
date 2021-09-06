#include<stdio.h>
void main()
{
    int a;
    printf("Enter the size of matrix:");
    scanf("%d",&a);
    printf("Enter the first matrix:--------------------\n");
    int arr[a][a];
    for (int i=0;i<a;i++)
    {printf("Enter the %d row:",i+1);
        for (int j=0;j<a;j++)
    {
        scanf("%d",&arr[i][j]);
    }
    }
    printf("The first matrix entered by you is:");
    for (int i=0;i<a;i++)
    {printf("\n");
        for (int j=0;j<a;j++)
            printf("%d\t",arr[i][j]);
    }
    printf("\nEnter second matrix:-----------------------\n");
    int arr1[a][a];
    for (int i=0;i<a;i++)
    {printf("Enter the %d row:",i+1);
        for (int j=0;j<a;j++)
    {
        scanf("%d",&arr1[i][j]);
    }
    }
    printf("The second matrix entered by you is:");
    for (int i=0;i<a;i++)
    {printf("\n");
        for (int j=0;j<a;j++)
            printf("%d\t",arr1[i][j]);
    }
    int mul[a][a];
    for (int k=0;k<a;k++)
        for(int i=0;i<a;i++)
        {mul[k][i]=0;
            for(int j=0;j<a;j++)
                {
                    mul[k][i]+=arr[k][j]*arr1[j][i];
                }
        }
    printf("\nThe matrix multiplication is:\n");
    for (int i=0;i<a;i++)
    {printf("\n");
        for (int j=0;j<a;j++)
            printf("%d\t",mul[i][j]);
    }
}
