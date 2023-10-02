
**Iterative Approach**
import java.util.Arrays;

public class ReverseArray {
	public static int[] reverseIteratively(int arr[], int length) {
		int s = 0, e = length - 1;
		while (s < e) {
			int temp = arr[s];
			arr[s] = arr[e];
			arr[e] = temp;
			s++;
			e--;
		}
		return arr;
	}

	public static void main(String[] args) {
		int arr[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9 };
		int len = arr.length;
		System.out.println("Original Array: " + Arrays.toString(arr));

		reverseIteratively(arr, len);
		System.out.println("Iterative Reverse: " + Arrays.toString(arr));
	}
}
