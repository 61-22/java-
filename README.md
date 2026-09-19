# java-
两数之和的哈希表做法  
import java.util.Map;  
import java.util.HashMap;  
  
class Solution{  
     public int[] twoSum(int nums[],int target){  
           Map<Integer,Integer> hashmap=new HashMap<>();  
              
           for(int i=0;i<nums.length;i++){  
              int curNum=nums[i];  
              int need=target-nums[i];  
                 if(hashmap.containsKey(need)){
                   return new int[]{hashmap.get(need),i};
                 }
                 hashmap.put(curNum,i);
           }
           //题目保证一定有解，兜底返回
           return new int[]{};
     }
}

     
