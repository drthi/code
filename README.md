public class Dograce {

	/**
	 * @param args
	 */
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int[] dog = new int [5]; 
		int numdogs, steps;
	
		numdogs= rNum (1,5);
		System.out.println(numdogs);
		System.out.println("dog   steptaken  totalsteps");
		steps = loopdog(numdogs,dog);
		finishrace(steps);
		diagram(dog,numdogs);
		
		
	}
	public static int rNum(int low, int high)
	{
		int random = (int )(Math.random() * high + low);
		return random;
	}
	
	public static int loopdog(int numdogs,int dog[])
	{
		
		int totalsteps;
		totalsteps = 0;
		for (int x=0; x<numdogs; x++)
		{
			
			dog[x]= rNum(0,30);
			totalsteps= totalsteps+ dog[x];

			System.out.print(x+1 + "        ");
			System.out.print(dog[x] + "        ");
			System.out.println(totalsteps);
		}
		return totalsteps;
	}
	
	public static void finishrace (int steps)
	{
		if (steps >= 75)
		{
			System.out.println("The dog has completed the race");
		}
		else 
		{
			System.out.println("The dog has not completed the race");
		}
	}
	
	public static void diagram (int dog[],int n)
	{
		for (int x=0; x<n; x++)
		{
			System.out.print("D" + x+1);
			for (int y=0; y<dog[x]; y++)
			{
				
				System.out.print("-");
			}
		}
	}
}
