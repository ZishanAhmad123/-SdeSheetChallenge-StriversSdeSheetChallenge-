#include<bits/stdc++.h>
using namespace std;
int compareVersions(string a, string b) 
{
    // Write your code here
    int n=a.size();
    int m=b.size();
    vector<long long> arr(n+1);
    vector<long long> arr2(m+1);
    long long  u=0;
     long long k=0;
    long long u1=0;
    long long k1=0;
    for(int i=0;i<n;i++)
    {
        if(a[i]>='0' && a[i]<='9')
        {
           long long p =(long long)a[i]-'0';
//             if(p==0 && u==0)
//             {
//                 k--;
//                 continue;
//             }
            u=u*10+p;
            arr[k]=u;
            
        }
        else if(a[i]=='.')
        {
            k++;
            u=0;
        }
    }
    for(int i=0;i<m;i++)
    {
         if(b[i]>='0' && b[i]<='9')
        {
           long long p =(long long)b[i]-'0';
//              if(p==0 && u1==0)
//             {
//                 k1--;
//                 continue;
//             }
            u1=u1*10+p;
            arr2[k1]=u1;
        }
        else if(b[i]=='.')
        {
            k1++;
            u1=0;
        }
    }
    int i=0;
    int j=0;
//     for(int l=0;l<=k;l++)
//         cout<<arr[l]<<" ";
//     cout<<endl;
    while(i<=k && j<=k1)
    {
        if(arr[i]< arr2[j])
        {
            return -1;
        }
        else if(arr[i]>arr2[j])
        {
            return 1;
        }
        i++;
        j++;
    }
   while(j<=k1)
   {
       if(arr2[j]==0)
       {
           j++;
           continue;
       }
       return -1;
   }
    while(i<=k)
    { 
        if(arr[i]==0)
        {
            i++;
            continue;
        }
        return 1;
    }
    return 0;
}
