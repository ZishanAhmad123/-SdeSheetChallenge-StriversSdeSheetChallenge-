bool is_pal(string s, int start, int end)
{
    int i=start,j=end;
    while (i<j)
    {
        if (s[i] != s[j])
        {
            return false;
        }
        i++;
        j--;
    }
    return true;
}

void helper(string s, int start, int end, vector<vector<string>> &res,
      vector<string>part)
{
    if (end == s.length())
    {
        if (start == end)
        {
            res.push_back(part);
        }
        return;
    }
    helper(s,start,end+1,res,part);
    if (is_pal(s,start,end))
    {
        part.push_back(s.substr(start,end-start+1));
        helper(s,end+1,end+1,res,part);
        part.pop_back();
    }
}

vector<vector<string>> partition(string &s) 
{
    vector<vector<string>>res;
    vector<string>part;
    helper(s,0,0,res,part);
    return res;
}
