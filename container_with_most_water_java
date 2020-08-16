class Solution {
    public int maxArea(int[] height) {
        int max = 0;
        
        for (int i = 0; i < height.length; i++)
            for (int j = i; j < height.length; j++) {
                if (i == j) continue;
                int cur = (j-i) * minHeight(height[i], height[j]);
                if (cur > max) max = cur;
            }
        
        return max;
    }
    
    private int minHeight(int h1, int h2){
        if (h1 < h2) return h1;
        else return h2;
    }
}
