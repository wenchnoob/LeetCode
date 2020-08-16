import java.util.Arrays;

class Solution {
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
        int[] arr = merge(nums1, nums2);
        
        if (arr.length % 2 != 0) {
            return arr[arr.length/2];
        } else {
            return (arr[arr.length/2] + arr[arr.length/2 - 1]) / 2.0;
        }
    }
    
    private int[] merge(int[] arr1, int[] arr2) {
        int[] aux = new int[arr1.length + arr2.length];
        int head1 = 0;
        int head2 = 0;
        
        for (int i = 0; i < aux.length; i++) {
            if (head1 >= arr1.length){
                aux[i] = arr2[head2++];
                continue;
            }
            
            if (head2 >= arr2.length) {
                aux[i] = arr1[head1++];
                continue;
            }
            
            if (arr1[head1] < arr2[head2]){
                aux[i] = arr1[head1++];
            } else {
                aux[i] = arr2[head2++];
            }
        }
        
        return aux;
    }
}
