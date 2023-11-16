# JavaCODE 🥀

                                                                      <h1>CODE IN JAVA😉<h1>

Love Babbar solutions 🤓🤓  !!  

 

REVERSE THE ARRAY
https://practice.geeksforgeeks.org/problems/reverse-a-string/1?utm_source=geeksforgeeks&utm_medium=ml_article_practice_tab&utm_campaign=article_practice_tab
class Reverse
{ 
    // Complete the function 
    // str: input  string
    public static String reverseWord(String str)
    {
        String ans="";
        for(int i=str.length()-1;i>=0;i--){
            ans+=str.charAt(i);
        }
        return ans;
   }
}

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

MIN AND MAXIMUM OF THE ARRAY
https://practice.geeksforgeeks.org/problems/max-min/1?utm_source=gfg&utm_medium=article&utm_campaign=bottom_sticky_on_article 

class Solution
{ 
    public static int findSum(int A[],int N) 
    {
       Arrays.sort(A);
       int min=A[0];
       int max=A[N-1];
       return min+max;
    }
}

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

KTH SMALLEST ELEMENT IN AN ARRAY

https://practice.geeksforgeeks.org/problems/kth-smallest-element5635/1

class Solution{
    public static int kthSmallest(int[] arr, int l, int r, int k) 
    { 
        Arrays.sort(arr);
        int kth=arr[k-1];
        return kth;
    } 
}



------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

SORT THE 0,1,2 IN AN ARRAY

https://practice.geeksforgeeks.org/problems/sort-an-array-of-0s-1s-and-2s4231/1

class Solution
{
    public static void sort012(int a[], int n)
    {   
       int i=0;
       int j=0;
       int k=n-1;
       
       while(i<=k){
           if(a[i]==0){
               swap(a,i,j);
               i++;
               j++;
           }else if(a[i]==1){
               i++;
           }else{
               swap(a,i,k);
               k--;
           }
       }
       
    }
    public static void swap(int[] arr,int i,int j){
        int temp=arr[i];
        arr[i]=arr[j];
        arr[j]=temp;
    }
}

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

MOVE ALL NEGATIVE ELEMENTS TO END

https://practice.geeksforgeeks.org/problems/move-all-negative-elements-to-end1813/1?utm_source=geeksforgeeks&utm_medium=ml_article_practice_tab&utm_campaign=article_practice_tab

class Solution {
    
    public void segregateElements(int arr[], int n)
    {
        ArrayList<Integer>neg=new ArrayList<>();
        ArrayList<Integer>pos=new ArrayList<>();
        for(int x:arr){
            if(x>0){
                pos.add(x);
            }else{
                neg.add(x);
            }
        }
        for(int i=0;i<n;i++){
            if(i<pos.size()){
                arr[i]=pos.get(i);
            }else{
                arr[i]=neg.get(i-pos.size());
            }
        }
    }
}

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

FIND UNION AND INTERSECTION OF  TWO SORTED  ARRAY 

https://practice.geeksforgeeks.org/problems/union-of-two-arrays3538/1

class Solution{
    public static int doUnion(int a[], int n, int b[], int m) 
    {
        HashSet<Integer>hs=new HashSet<>();
        for(int x:a){
            hs.add(x);
        }
        for(int x:b){
            hs.add(x);
        }
        return hs.size();
    }
}

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

CYCLICALLY ROTATE AN ARRAY BY ONE

https://practice.geeksforgeeks.org/problems/cyclically-rotate-an-array-by-one2614/1

class Compute {
    
    public void rotate(int arr[], int n)
    {
        int last=arr[n-1];
        for(int i=0;i<n;i++){
            int temp=last;
            last=arr[i];
            arr[i]=temp;
        }
    }
}

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

MAXIMUM SUBAARRAY SUM

https://practice.geeksforgeeks.org/problems/kadanes-algorithm-1587115620/1


class Solution{

    // arr: input array
    // n: size of array
    //Function to find the sum of contiguous subarray with maximum sum.
    long maxSubarraySum(int arr[], int n){
        
        long currsum=0;
        long maxsum=Integer.MIN_VALUE;
         for(int i=0;i<n;i++){
             currsum+=arr[i];
             if(currsum>maxsum){
                 maxsum=currsum;
             }
         if(currsum<0){
             currsum=0;
            }
        }
         return maxsum;
        
    }
    
}


---------------------------------------------------------------------------------------------------------------------------------------------------------------------

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

MINIMIZE THE HEIGHTS II

https://practice.geeksforgeeks.org/problems/minimize-the-heights3351/1

class Solution {
    int getMinDiff(int[] arr, int n, int k) {
        if(n==1)return 0;
        
        Arrays.sort(arr);
        
        int diff=arr[n-1]-arr[0];
        int min,max;
        for(int i=1;i<n;i++){
            if(arr[i]-k<0)
            continue;
            
            max=Math.max(arr[i-1]+k,arr[n-1]-k);
            min=Math.min(arr[0]+k,arr[i]-k);
            diff=Math.min(diff,max-min);
        }
        return diff;
    }
}

-----------------------------------------------------------------------------------------------------------------------------------------------------------------

MINIMUM NUMBER OF JUMPS

https://practice.geeksforgeeks.org/problems/minimum-number-of-jumps-1587115620/1

class Solution{
    static int minJumps(int[] arr){
        // your code here
        int currReach=0,currmax=0,jump=0;
        int n=arr.length;
        for(int i=0;i<n-1;i++){
            if(i+arr[i]>currmax)
                currmax=arr[i]+i;
                if(i==currReach){
                    jump++;
                    currReach=currmax;
        }
            if(arr[i]==0 && i==currmax)return -1;
        }
        return jump;
    }
}

------------------------------------------------------------------------------------------------------------------------------------------------------------------

FIND THE DUPLICATE NUMBER

https://leetcode.com/problems/find-the-duplicate-number/


class Solution {
    public int findDuplicate(int[] nums) {
    HashSet<Integer>hs=new HashSet<>();
    for(int x:nums){
        if(hs.contains(x)){
            return x;
        }else{
            hs.add(x);
        }
    }
    return -1;
}
}


-----------------------------------------------------------------------------------------------------------------------------------------------------------------


