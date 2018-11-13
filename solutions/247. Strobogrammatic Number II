/*

Same recusion framework as word breaker II, bottom up reconstruction.
Note the way to handle "00"


*/
class Solution {
public:
    vector<string> dfs(int n, int cnt) {
        if(n == 0){
            vector<string> res;
            res.push_back(""); // base case for n=2*k, if no "", recusion won't happen!
            return res;
        }
        else if(n == 1) { // base case for n=2*k+1
            vector<string> res;
            res.push_back("0");
            res.push_back("1");
            res.push_back("8");
            return res;
        } else {
            vector<string> tmp;
            vector<string> res = dfs(n-2, cnt);
            for(auto s : res) {
                if (n != cnt) tmp.push_back("0" + s + "0"); //avoid putting 0 to the head
                tmp.push_back("6" + s + "9");
                tmp.push_back("9" + s + "6");
                tmp.push_back("8" + s + "8");
                tmp.push_back("1" + s + "1");
            }
            return tmp;
        }
    }
    vector<string> findStrobogrammatic(int n) {
        return dfs(n, n);
    }
};
