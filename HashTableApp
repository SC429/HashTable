import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

public class HashTableApp {

	// Builds and returns a hash table of frequencies from the given input file
	public static HashSeparateChaining getMap(Scanner in){
		HashSeparateChaining map = new HashSeparateChaining();

		while(in.hasNext()){
			String word = in.next(); // read next word in file
			word = word.toLowerCase();
			
			if (map.get(word) != null) { // check to see if the key is the table
				int freq = map.get(word); // get the initial frequency
				freq++; //increment the frequency
				map.put(word, freq); // insert word with frequency
			}
			else {
				map.put(word, 1); // if the word doesn't exist in the table
			}
		}
		return map;
	}

	public static void main(String[] args) {
		if (args.length < 1){
			System.out.println("Pass the filename to be read as an argument.");
			System.exit(-1);
		}

		File input = new File(args[0]);
		Scanner fileReader = null;

		try{
			fileReader = new Scanner(input);
		} catch (FileNotFoundException e) {
			System.out.println("File was not found.  Check the file name and try again.");
			System.exit(-2);
		}

		HashSeparateChaining map = getMap(fileReader);
		System.out.println(map); // invokes map.toString()
	}
}
