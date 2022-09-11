# Migratory-BIrds-Hackerrank
this is problem statement from hackerrank

#include <stdio.h>

int main()
{
    int n,i;
    scanf("%d",&n);
    int arr[n];
    int count[5]={0};
    for(i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
        count[arr[i]-1]++;
    }
    int max = count[0];
    int max_index=0;
    for(i=1;i<5;i++)
    {
        if(count[i]>max)
        {
            max=count[i];
            max_index=i+1;
        }
    }
    printf("%d",max_index);
    return 0;
}
