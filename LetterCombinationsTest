import java.util.ArrayList;
import java.util.List;

/**
 * <p>Happy Valentine's Day! :)</p>
 * Input: arr[] = {2, 3}
 * Output: ad ae af bd be bf cd ce cf
 *
 *  * Input: arr[] = {9}
 *  * Output: w x y z
 *
 * @author fengbz
 * @date 2020/02/14
 */
public class LetterCombinationsTest {

    private static final String[] LETTERS = {"", "", "abc", "def", "ghi", "jkl", "mno", "pqrs", "tuv", "wxyz"};

    public static void main(String[] args) {
        int[] inputNums = {2, 3};
        List<String> ret = new LetterCombinationsTest().letterCombinations(inputNums);

        System.out.print("Example 1: ");
        for (int i = 0; i < ret.size(); i++) {
            System.out.print(ret.get(i) + " ");
        }
        System.out.println();

        int[] inputNums2 = {9};
        List<String> ret2 = new LetterCombinationsTest().letterCombinations(inputNums2);

        System.out.print("Example 2: ");
        for (int i = 0; i < ret2.size(); i++) {
            System.out.print(ret2.get(i) + " ");
        }

        System.out.println();

        System.out.println("======Stage 2 ?======");
        int[] inputNums3 = {2, 99};
        List<String> ret3 = new LetterCombinationsTest().letterCombinations(inputNums3);

        System.out.print("Example 3: ");
        for (int i = 0; i < ret3.size(); i++) {
            System.out.print(ret3.get(i) + " ");
        }
    }

    public List<String> letterCombinations(int[] inputNums) {
        List<String> list = new ArrayList<>();
        if (inputNums == null || inputNums.length == 0) {
            return list;
        }
        String currentStr = "";
        addLetter(join(inputNums), 0, list, currentStr);
        return list;
    }

    private static void addLetter(String inputNums, int index, List<String> list, String currentStr) {
        if (index == inputNums.length()) {
            list.add(currentStr);
            return;
        }
        char[] letters = getLetters(Integer.parseInt(String.valueOf(inputNums.charAt(index))));

        if (letters == null) {
            list.add(currentStr);
            return;
        }

        for (int i = 0; i < letters.length; i++) {
            addLetter(inputNums, index + 1, list, currentStr + letters[i]);
        }
    }

    private static char[] getLetters(int num) {
        if (num == 0 || num == 1) {
            return null;
        }
        return LETTERS[num].toCharArray();
    }

    private static String join(int[] nums) {
        String ret = "";
        if (nums == null || nums.length == 0) {
            return ret;
        }

        for (int i = 0; i < nums.length; i++) {
            ret += nums[i];
        }

        return ret;
    }
}
