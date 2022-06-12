void helper(vector<int> &num,vector<int> &sumArr,int sum,int index)

{

   if(index<0) {

       sumArr.push_back(sum);

       return;

   }

   

   helper(num,sumArr,sum,index-1);

   helper(num,sumArr,sum+num[index],index-1);    

}

vector<int> subsetSum(vector<int> &num)

{

   // Write your code here.

   vector<int> sumArr;

   helper(num,sumArr,0,num.size()-1);

   sort(sumArr.begin(),sumArr.end());

   return sumArr;

}
