//

class Solution {
public:
    bool uniqueOccurrences(vector<int>& arr) {
        vector<int>ans;
        sort(arr.begin(),arr.end());
        int i = 0;
        while(i<arr.size()){     
            int count =1;
        for(int j=i+1;j<arr.size();j++){
            if(arr[i]==arr[j]){
                    count++;
            }
            else{
                break;
            }
         
        }
   ans.push_back(count);
            i=i+count;
        }
    int size = ans.size();
    sort(ans.begin(),ans.end());
    for(int i=0;i<size-1;i++){
        if(ans[i] == ans[i+1]){
            return false;
        }
    }
    return true;
    }
};
