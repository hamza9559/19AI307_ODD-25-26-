# Ex.No:3(b) POLYMORPHISM

## QUESTION:
```
Create a base class BankAccount with methods deposit() and withdraw().
Create two subclasses:
SavingsAccount: allows withdrawal but limits it to ₹10,000 per transaction.
CheckingAccount: allows withdrawal with a ₹10 fee per transaction.
Input account type, deposit amount, and withdrawal amount from the user.
If checking account has insufficient balance print - "Insufficient balance in CheckingAccount (including ₹10 fee)."
```

## AIM:
To implement inheritance in banking accounts by applying different withdrawal rules for SavingsAccount and CheckingAccount.

## ALGORITHM :
1.	Start the program and read the account type, deposit amount, and withdrawal amount.
2. Create a base class BankAccount with deposit and withdraw methods.
3. Create SavingsAccount and CheckingAccount subclasses with specific withdrawal rules.
4. Create the correct account object based on the user input type.
5. Perform deposit and withdrawal operations according to account rules.
6. Display the final balance or an appropriate message if withdrawal fails.




## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;

class BankAccount {
    double balance;

    void deposit(double amount) {
        balance += amount;
        System.out.println("Deposited: ₹" + amount);
    }

    void withdraw(double amount) {}
}

class SavingsAccount extends BankAccount {
    @Override
    void withdraw(double amount) {
        if (amount > 10000) {
            System.out.println("Withdrawal limit for SavingsAccount is ₹10,000 per transaction.");
        } else if (amount > balance) {
            System.out.println("Insufficient balance in SavingsAccount.");
        } else {
            balance -= amount;
            System.out.println("Withdrawn from SavingsAccount: ₹" + amount);
        }
    }
}

class CheckingAccount extends BankAccount {
    final double FEE = 10.0;

    @Override
    void withdraw(double amount) {
        if (amount + FEE > balance) {
            System.out.println("Insufficient balance in CheckingAccount (including ₹10 fee).");
        } else {
            balance -= (amount + FEE);
            System.out.println("Withdrawn from CheckingAccount: ₹" + amount + " (₹10 fee applied)");
        }
    }
}

public class BankSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String type = sc.nextLine().trim().toLowerCase();
        double depositAmount = sc.nextDouble();
        double withdrawAmount = sc.nextDouble();

        BankAccount account;

        if (type.equals("savings")) {
            account = new SavingsAccount();
        } else if (type.equals("checking")) {
            account = new CheckingAccount();
        } else {
            System.out.println("Invalid account type.");
            sc.close();
            return;
        }

        account.deposit(depositAmount);
        account.withdraw(withdrawAmount);
        System.out.printf("Final Balance: ₹%.2f\n", account.balance);

        sc.close();
    }
}

```






## OUTPUT:
<img width="1288" height="503" alt="image" src="https://github.com/user-attachments/assets/cde59034-eeda-4ac5-91eb-4ee120a2e581" />



## RESULT:
Thus, the program executed successfully and displayed the correct output based on the given input and conditions.
