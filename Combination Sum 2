class Solution {
    public List<List<Integer>> combinationSum2(int[] candidates, int target) {
        List<List<Integer>> result = new ArrayList<>();
        Arrays.sort(candidates);
        f(candidates, target, 0, new ArrayList<>(), result);
        return result;    
    }
    static void f(int[] candidates, int target, int ind, List<Integer> list, List<List<Integer>> result) {
        if (target == 0) {
            result.add(new ArrayList<>(list));
            return;
        }

        if (target < 0) return;
        
        for (int i = ind; i < candidates.length; i++) {
            if (i > ind && candidates[i] == candidates[i - 1]) {
                continue;
            }
            list.add(candidates[i]);
            f(candidates, target - candidates[i], i + 1, list, result);
            list.remove(list.size() - 1);
        }
    }
}
