## [Problem Link](https://www.interviewbit.com/problems/length-of-last-word/)

## Solution
```cpp
int Solution::lengthOfLastWord(const string A) {
    int cnt=0;
    int i=A.length()-1;
    while(A[i]==' ')i--;
    while(i>=0&&A[i]!=' ') cnt++,i--;
    
    return cnt;
}
````
