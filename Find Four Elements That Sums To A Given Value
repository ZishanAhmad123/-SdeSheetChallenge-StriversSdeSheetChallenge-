#include <bits/stdc++.h> 
string fourSum(vector<int> arr, int target, int n) {
    // Write your code here.
    sort(arr.begin(),arr.end());
    for(int i=0;i<n;i++){
        for(int j=n-1;j>i;j--){
            
            long long p=target-arr[i]-arr[j];
            int left=i+1;
            int right=j-1;
            while(left<right){
                if(p==arr[left]+arr[right]){
                    return "Yes";
                }
                else{
                    if(arr[left]+arr[right]>p)right--;
                    else left++;
                }
            }
        }
    }
    return "No";
}
