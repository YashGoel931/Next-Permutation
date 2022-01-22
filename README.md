class Solution {
    public void nextPermutation(int[] a) {
     int n=a.length;
     int i=0,l=0;
     for(i=n-1 ; i>0 ; i--){
         if(a[i]>a[i-1])
           {l=i;break;}
     }
     if(l==0){
      Arrays.sort(a);
     }
     else{
         for(int j=n-1 ; j>=l ; j--){
          if(a[j]>a[l-1]){
            i=a[l-1];
            a[l-1]=a[j];
            a[j]=i;
            break;
          }    
         }
      Arrays.sort(a,l,n);
     }
    }
}
