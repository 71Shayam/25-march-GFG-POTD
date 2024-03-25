 void help(vector<string> &ans,int zero,int one,string temp,int N){
        if(temp.length()==N){
            ans.push_back(temp);
            return;
        }
        if(one>zero)help(ans,zero+1,one,temp+'0',N);
        help(ans,zero,one+1,temp+'1',N);
        
    }
	vector<string> NBitBinary(int n)
	{
	    // Your code goes here
	    vector<string> ans;
	    help(ans,0,1,"1",n);
	    sort(ans.begin(),ans.end());
	    reverse(ans.begin(),ans.end());
	    return ans;
	}
