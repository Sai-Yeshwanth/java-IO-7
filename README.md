import java.io.File;
import java.io.FileReader;
import java.io.IOException;
import java.io.BufferedReader;

public class Jala {
	public static void main(String[] args) throws IOException 
  {
		File file = new File("myfile.txt");
		BufferedReader br = new BufferedReader(new FileReader(file));
		try
        {
            String line;
            while ((line = br.readLine()) != null) 
            {
                System.out.println(line);
            } 
        }
         catch (IOException e) {
            System.out.println("Sorry!!! can't read the file");;
        }
        br.close();
   }
}
