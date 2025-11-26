# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to create a new file and write user-provided content into it.

## AIM:
To create a new file and write user-provided content into it using Java I/O classes.

## ALGORITHM :
1.	Start the program and create a Scanner object to read input from the user.
2. Read the file name and the content to be written.
3. Create a File object with the given file name.
4. Check if the file already exists; if not, create a new file.
5. Use FileWriter to write the user-provided content into the file.
6. Close the writer and display a success message or handle exceptions if any occur.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:
```JAVA
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;
import java.io.File;

public class CreateAndWriteFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String fileName = sc.nextLine();
        String content = sc.nextLine();

        try {
            File file = new File(fileName);

            if (file.createNewFile()) {
                System.out.println("File created: " + file.getName());
            } else {
                System.out.println("File already exists. Writing content...");
            }

            FileWriter writer = new FileWriter(file);
            writer.write(content);
            writer.close();

            System.out.println("Content written to the file successfully.");

        } catch (IOException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }

        sc.close();
    }
}
```






## OUTPUT:

<img width="1214" height="440" alt="image" src="https://github.com/user-attachments/assets/5a82c95e-1053-4ce4-ab1e-fc0a000ef1ee" />



## RESULT:
The program executed successfully and created a new file (or used an existing one) and wrote the provided content into it.
