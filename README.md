# 771.-Jewels-and-Stones

`````c#
You're given strings J representing the types of stones that are jewels, and S representing the stones you have.  Each character in S is a type of stone you have.  You want to know how many of the stones you have are also jewels.

The letters in J are guaranteed distinct, and all characters in J and S are letters. Letters are case sensitive, so "a" is considered a different type of stone from "A".

Solution 1: 
public class Solution {
    public int NumJewelsInStones(string J, string S) {
       
        int res = 0;
         
        for(int i = 0; i< S.Length; i++)
        {
            if(J.IndexOf(S[i]) > -1){
                ++res;
            }
        }
        
        return res;
        
    }
}

T(n) = O(n)

Solution 2:

public class Solution {
    public int NumJewelsInStones(string J, string S) {
       
        int res = 0;
        for(int i=0; i<J.Length; i++){
            for(int j=0; j<S.Length; j++){
                
                if(J[i] == S[j]){
                    res +=1;
                }
            }
        }
        
        return res;
        
    }
}

T(n) = O(n^2)




`````
