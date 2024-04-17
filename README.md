# 75
class Solution {
public:
    void setZeroes(vector<vector<int>>& matrix) {
        vector<bool> ro(matrix.size(), false);
       vector<bool> co(matrix[0].size(), false);
        for(int i=0;i<matrix.size();i++){
            for(int j=0;j<matrix[0].size();j++){
                if(matrix[i][j]==0){
                    ro[i]=true;
                    co[j]=true;
                }
            }
        }
        for(int i=0;i<matrix.size();i++){
            for(int j=0;j<matrix[0].size();j++){
                if(ro[i]|| co[j]){
                    matrix[i][j]=0;
                    
                }

            }
        }
    }
};
