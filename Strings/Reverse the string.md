## [Problem Link](https://www.interviewbit.com/problems/reverse-the-string/)

### Solution

```cpp
  string Solution::solve(string A) {
    stringstream ss(A);
        string word,res;
        while(ss>>word)
        {
            res=word+" "+res;
        }
        res.pop_back();
        return res;
      }
````

## approach-2(TLE)
```cpp
string Solution::solve(string A) {
stack<char> s;
int n = A.size();
string add="";
int i= n-1;

while(i>=0)
{
    while(isspace(A[i])==1 && i>=0) i--;
    
    while(isspace(A[i])==0 && i>=0)
       { s.push(A[i]);i--;}
    
    while(!s.empty())
    {
        add = add + s.top();
        s.pop();
    }
    add = add + " ";
}
add.pop_back();
if(add[add.length()-1]==' ')add.pop_back();
return add;
}
`````
