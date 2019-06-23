# ArryaBubbleSort

#Practice 

Array Buuble sort 

/Ramin Roufeh
//Array Example practice


public class ArrayExample {
	public static void main(String[] args){
		int[] list = {1,2,3,4,5,2,4,5};
		int target = 4;
		search(list, target);
		bubblesort(list);
		showList(list);
		

		list = new int[]{11, 10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0, -1, -2};
		bubblesort(list);
		showList(list);

		list = new int[]{1,9,8,76,5,4,3,2,23,45};
		bubblesort(list);
		showList(list);
		
	}
	
	public static void search(int[] list, int target)
	{	
		assert list != null : "failed precondition";

			for(int i = 0; i < list.length; i++)
				
			{	if(list[i] == target)
				{	System.out.println("The target " + target + " is in " + 
						+ (i+1) + " in the list");
				}
			}
		
	}
	
	public static void bubblesort(int list[]) {
		
		int n = list.length;
		
		for(int i=0; i<n-1;i++)
			for(int j=0;j<n-1-1; j++)
				if(list[j]>list[j+1]) {
					//swap list[j+1] and arr[i]
					int temp = list[j];
					list[j] = list[j+1];
					list[j+1] = temp;
				}
	}

	public static void showList(int[] list)
	{	for(int i = 0; i < list.length; i++)
			System.out.print( list[i] + " " );
		System.out.println();
	}

	
}



//Output

The target 4 is in 4 in the list
The target 4 is in 7 in the list
1 2 2 3 4 4 5 5 
-1 0 1 2 3 4 5 6 7 8 9 10 11 -2 
1 2 3 4 5 8 9 23 76 45 
