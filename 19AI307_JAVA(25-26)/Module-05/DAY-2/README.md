# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:

Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.
## AIM:

To serialize and deserialize a collection of Student objects into/from a file using Java I/O.
## ALGORITHM :
1.	Start the program and create a Student class implementing Serializable.
2. Read the number of students and their details (id, name, marks) from the user.
3. Store all student objects in an ArrayList<Student>.
4. Use ObjectOutputStream to serialize the list into a file.
5. Use ObjectInputStream to deserialize the list from the file.
6. Display the deserialized student objects to verify successful serialization and deserialization.





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:
```JAVA
import java.io.*;
import java.util.*;


class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {


    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

   
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); 

        
        
        // Write your code here
        for (int i = 0; i < n; i++) {
            int id = scanner.nextInt();
            scanner.nextLine(); 
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            if (scanner.hasNextLine()) scanner.nextLine(); 

            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";

     
        serializeStudents(students, fileName);

      
        List<Student> deserializedStudents = deserializeStudents(fileName);


        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}


```




## OUTPUT:


<img width="1274" height="538" alt="image" src="https://github.com/user-attachments/assets/1aba6afd-fa1a-4b31-aef9-d155a09f3eb5" />


## RESULT:

The program executed successfully, serialized the list of students into a file, deserialized it back, and displayed all student details correctly.
