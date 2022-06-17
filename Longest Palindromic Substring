int expand(string& s, int left, int right){
    while(left>=0 and right<s.length() and s[left]==s[right]){
        left--;
        right++;
    }
    return right-left-1;
}
string longestPalinSubstring(string str)
{
    int start = 0, end = 0;
    int maxLen = 0;
    for(int i=0;i<str.length();i++){
        int odd = expand(str, i, i);
        int even = expand(str, i, i+1);
        
        int len = max(odd, even);
        if(maxLen<len){
            maxLen = len;
            start = i - (len-1)/2;
            end = i + (len)/2;
        }
    }
    return str.substr(start, maxLen);
}
