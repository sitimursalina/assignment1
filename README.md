import java.io.BufferedWriter;
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;

public class sitimursalinatxt {
	public static void main(String[] args) {
		try {

			String name = "Name:Siti Mursalina";
			String matrixno = "StudID:2014667262";
			String gender = "Gender:Female";
			String age = "Age:31";
			String email = "Email:sitimursalina@unikl.edu.my";
			String hpno = "HPNo:0169099258";
			

			File file = new File("mursalina.txt");

			// if file doesnt exists, then create it
			if (!file.exists()) {
				file.createNewFile();
			}

			FileWriter fw = new FileWriter(file.getAbsoluteFile());
			BufferedWriter bw = new BufferedWriter(fw);
			bw.write(name);
			bw.newLine();
			bw.write(matrixno);
			bw.newLine();
			bw.write(gender);
			bw.newLine();
			bw.write(age);
			bw.newLine();
			bw.write(email);
			bw.newLine();
			bw.write(hpno);
			bw.close();

			System.out.println("Done");

		} catch (IOException e) {
			e.printStackTrace();
		}
	}
}
