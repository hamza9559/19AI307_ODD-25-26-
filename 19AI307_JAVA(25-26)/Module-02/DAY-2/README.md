# Ex.No:2(B) METHODS

## QUESTION:
```
Write a class with one static method and one non-static method. Call both from the main() method.
When staticMethod() is called, it should print  "I am static".
When nonStaticMethod() is called, it should print  "I am non-static"
```
## AIM:
To create a class with a static method and a non-static method and call both from the main method.

## ALGORITHM :
1.	Define a class with one static and one non-static method.
2. Print a message inside the static method.
3. Print a message inside the non-static method.
4. Call the static method directly using the class name.
5. Create an object to call the non-static method and display its message.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:

```JAVA
class MyClass {
    static void staticMethod() {
        System.out.println("I am static");
    }

    void nonStaticMethod() {
        System.out.println("I am non-static");
    }
}

class prog {
    public static void main(String[] args) {
        MyClass.staticMethod();

        MyClass obj = new MyClass();
        obj.nonStaticMethod();
    }
}

```





## OUTPUT:

<img width="1221" height="262" alt="image" src="https://github.com/user-attachments/assets/f7167e9d-bdc6-40c7-ba26-54074f33d746" />


## RESULT:

Thus, the program executed successfully and displayed the correct output based on the given input and conditions.
