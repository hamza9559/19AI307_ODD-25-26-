# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a Java program to write a string to a text file named output.txt.

## AIM:

To write a given string into a text file named output.txt using Java I/O.
## ALGORITHM :
1.	Start the program and define the string data to be written.
2. Create a FileWriter object for the file output.txt.
3. Use the write() method of FileWriter to write the string into the file.
4. Close the FileWriter to release system resources.
5. Handle any IOException that may occur during file operations.
6. Display a success message after writing the content.




## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:

```JAVA
import java.io.FileWriter;
import java.io.IOException;

public class WriteStringToFile {
    public static void main(String[] args) {
        String data = "This is the content to write into the file.";

        try {
            FileWriter writer = new FileWriter("output.txt");
            writer.write(data);
            writer.close();
            System.out.println("Successfully wrote to the file.");
        } catch (IOException e) {
            System.out.println("An error occurred while writing to the file.");
        }
    }
}
```





## OUTPUT:

<img width="1280" height="272" alt="image" src="https://github.com/user-attachments/assets/41315770-3947-44eb-91e1-7b7551ed65a1" />



## RESULT:
RESULT

The program executed successfully and wrote the specified string into output.txt.
