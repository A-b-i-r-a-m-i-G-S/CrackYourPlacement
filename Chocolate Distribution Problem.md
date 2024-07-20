Given an array A[ ] of positive integers of size N, where each value represents the number of chocolates in a packet. Each packet can have a variable number of chocolates. There are M students, the task is to distribute chocolate packets among M students such that :
1. Each student gets exactly one packet.
2. The difference between maximum number of chocolates given to a student and minimum number of chocolates given to a student is minimum

```
class Solution
{
    public long findMinDiff (ArrayList<Integer> a, int n, int m)
    {
        Collections.sort(a);
        // 1 3 4 7 9 9 12 56
        
        int i = 0;
        int diff = a.get(n-1);
        
        for(int j=m-1;j<n;j++){
            diff = Math.min(diff, a.get(j) - a.get(i));
            i++;
        }
        
        return diff;
    }
}
```
