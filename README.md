import java.util.ArrayList;
import java.util.Collections;
import java.util.Iterator;
//Write java programs showing following functionalities using an ArrayList.

public class Col1 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		/* to create a new array list containing student names, 
		add some student (string) and print out the collection.  */
		ArrayList<String> std = new ArrayList<String>();
		std.add("Sandeep");
		std.add("Shankar");
		std.add("Abhi");
		std.add("Yogi");
		
		System.out.println(std);
		
		//to iterate through all elements in a array list.
		
		Iterator i = std.iterator();
		while(i.hasNext()) {
			System.out.println(i.next());
		}
		
		//to insert an element into the array list at the first position
		std.add(0, "Boss");
		std.add(5, "Vishnu" );
		System.out.println(std);
		
		//to retrieve an element (at a specified index) from a given array list.
		
		String ret = std.get(5);
		System.out.println(ret);
		ret = std.get(3);
		System.out.println(ret);
		
		//to update specific array element by given element
		
		std.set(3, "Dums");
		System.out.println(std);
		
		//to remove the third element from a array list.
		
		std.remove(3);
		System.out.println(std);
		
		//to search an element in a array list.
		if (std.contains("Yogi"))
		{
			System.out.println("found in the list");
		}
		else
		{
		System.out.println("Not found in the list");
		}
		
		//to sort a given array list.
		System.out.println("List before sort "+std);
		Collections.sort(std);
		System.out.println("List after sort "+std);
		
		//to copy one array list into another.
		ArrayList a = new ArrayList();
		a.add("1");
		a.add("2");
		a.add("3");
		a.add("4");
		a.add("5");
		Collections.copy(a, std);
		System.out.println(a);
		
		//to reverse elements in a array list.
		Collections.reverse(std);
		System.out.println(std);
		
		//to join two array lists.
		
		std.addAll(a);
		System.out.println(std);
		
		//to clone an array list to another array list.
		ArrayList cl = (ArrayList)a.clone();
		System.out.println("after cloning "+cl);
		
		//to empty an array list.
		std.removeAll(std);
		System.out.println("After remove "+std);
		
		//to test an array list is empty or not.
		System.out.println("Array list std is Empty? "+std.isEmpty());
	}

}
