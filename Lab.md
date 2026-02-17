
1. **WAP to print “Hello World” and explain the structure of a Java program.**
```java 
class HelloWorld {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```

2. **WAP to demonstrate command-line compilation and execution of a Java program.**
```java 
class CompileRun {
  public static void main(String[] args) {
    System.out.println("Java program compiled and executed successfully");
  }
}
```
`javac CompileRun.java`
`java CompileRun`

3. **WAP to find the maximum among three numbers using conditional statements.**
```java 
import java.util.Scanner;

class MaxOfThree {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int a = sc.nextInt();

        System.out.print("Enter second number: ");
        int b = sc.nextInt();

        System.out.print("Enter third number: ");
        int c = sc.nextInt();

        int max;

        if (a >= b && a >= c) {
            max = a;
        } else if (b >= a && b >= c) {
            max = b;
        } else {
            max = c;
        }

        System.out.println("Maximum number is: " + max);
    }
}
```
4. **WAP to print first *n* prime numbers (n from user).**
```java 
import java.util.Scanner;

class PrimeNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int count = 0, num = 2;

        while (count < n) {
            boolean prime = true;
            for (int i = 2; i <= num / 2; i++) {
                if (num % i == 0) {
                    prime = false;
                    break;
                }
            }
            if (prime) {
                System.out.print(num + " ");
                count++;
            }
            num++;
        }
    }
}

```
5. **WAP to generate Fibonacci series up to *n* terms.**
```java
import java.util.Scanner;

class Fibonacci {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        int a = 0, b = 1;
        System.out.print(a + " " + b + " ");
        for (int i = 3; i <= n; i++) {
            int c = a + b;
            System.out.print(c + " ");
            a = b;
            b = c;
        }
    }
}

```
6. **WAP to compute factorial of a given number.**
```java
import java.util.Scanner;

class Factorial {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        long fact = 1;

        for (int i = 1; i <= n; i++) {
            fact *= i;
        }
        System.out.println("Factorial: " + fact);
    }
}
```

7. **WAP to calculate sum of series: 1, 6, 9, 13, 17 … up to *n* terms.**
```java 
import java.util.Scanner;

class SeriesSum {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int sum = 0, term = 1;

        for (int i = 1; i <= n; i++) {
            sum += term;
            term += 4;
        }
        System.out.println("Sum = " + sum);
    }
}

```

8. **WAP to sort a list of numbers in ascending order using an array.**
```java
import java.util.Scanner;

class SortArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] a = new int[n];

        for (int i = 0; i < n; i++)
            a[i] = sc.nextInt();

        for (int i = 0; i < n - 1; i++)
            for (int j = i + 1; j < n; j++)
                if (a[i] > a[j]) {
                    int temp = a[i];
                    a[i] = a[j];
                    a[j] = temp;
                }

        for (int i : a)
            System.out.print(i + " ");
    }
}
```

9. **WAP to create a class `Student` with data members and methods to display details.**
```java 
class Student {
    // Data members
    int id;
    String name;
    float marks;

    // Method to display student details
    void displayDetails() {
        System.out.println("Student ID: " + id);
        System.out.println("Student Name: " + name);
        System.out.println("Marks: " + marks);
    }

    public static void main(String[] args) {
        // Creating first student object
        Student s1 = new Student();
        s1.id = 101;
        s1.name = "Ram";
        s1.marks = 85.5f;
        s1.displayDetails();

        System.out.println();

        // Creating second student object
        Student s2 = new Student();
        s2.id = 102;
        s2.name = "Sita";
        s2.marks = 92.0f;
        s2.displayDetails();
    }
}
```

10. **WAP to demonstrate default and parameterized constructors.**
```java 
class Student {

    int id;
    String name;

    // Default Constructor
    Student() {
        id = 0;
        name = "Not Assigned";
        System.out.println("Default Constructor Called");
    }

    // Parameterized Constructor
    Student(int i, String n) {
        id = i;
        name = n;
        System.out.println("Parameterized Constructor Called");
    }

    void display() {
        System.out.println("ID: " + id);
        System.out.println("Name: " + name);
    }

    public static void main(String[] args) {

        // Calling Default Constructor
        Student s1 = new Student();
        s1.display();

        System.out.println();

        // Calling Parameterized Constructor
        Student s2 = new Student(101, "Ram");
        s2.display();
    }
}
```
11. **WAP to calculate area and volume of a sphere using a class.**
```java 
class Sphere {
    double r;

    Sphere(double r) {
        this.r = r;
    }

    void display() {
        System.out.println("Area: " + (4 * Math.PI * r * r));
        System.out.println("Volume: " + ((4.0 / 3) * Math.PI * r * r * r));
    }

    public static void main(String[] args) {
        Sphere s = new Sphere(5);
        s.display();
    }
}

```
12. **WAP to demonstrate method overloading.**
```java 
class Overload {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }

    public static void main(String[] args) {
        Overload o = new Overload();
        System.out.println(o.add(2, 3));
        System.out.println(o.add(2.5, 3.5));
    }
}
```

13. **WAP to calculate factorial using recursion.**
```java 
class RecursionFact {
    static int fact(int n) {
        if (n == 1) return 1;
        return n * fact(n - 1);
    }

    public static void main(String[] args) {
        System.out.println(fact(5));
    }
}
```

14. **WAP to demonstrate single inheritance using `extends` keyword.**
```java 
// Parent class
class Employee {
    int id;
    String name;

    void displayEmployee() {
        System.out.println("Employee ID: " + id);
        System.out.println("Employee Name: " + name);
    }
}

// Child class - Full Time Employee
class FullTimeEmployee extends Employee {
    double monthlySalary;

    void displayFullTime() {
        displayEmployee();
        System.out.println("Monthly Salary: " + monthlySalary);
    }
}

// Child class - Part Time Employee
class PartTimeEmployee extends Employee {
    double hourlyRate;
    int hoursWorked;

    void displayPartTime() {
        displayEmployee();
        System.out.println("Hourly Rate: " + hourlyRate);
        System.out.println("Hours Worked: " + hoursWorked);
    }
}

class InheritanceDemo {
    public static void main(String[] args) {

        FullTimeEmployee f = new FullTimeEmployee();
        f.id = 101;
        f.name = "Ram";
        f.monthlySalary = 50000;
        f.displayFullTime();

        System.out.println();

        PartTimeEmployee p = new PartTimeEmployee();
        p.id = 102;
        p.name = "Sita";
        p.hourlyRate = 500;
        p.hoursWorked = 20;
        p.displayPartTime();
    }
}
```
15. **WAP to demonstrate method overriding and use of `super` keyword.**
```java 
class University {
    public void display() {
        System.out.println("Tribhuwan University");
    }
}

class College extends University {

    public void display() {
        super.display();  
        System.out.println("GoldenGate International College");
    }

    public static void main(String[] args) {
        College c = new College();
        c.display();
    }
}
```
16. **WAP to define and implement an interface.**
```java 
interface Shape {
    void calculateArea();
}

class Circle implements Shape {
    double radius = 5;

    public void calculateArea() {
        double area = 3.14 * radius * radius;
        System.out.println("Area of Circle: " + area);
    }

    public static void main(String[] args) {
        Circle c = new Circle();
        c.calculateArea();
    }
}
```
17. **WAP to handle arithmetic exception using try-catch-finally.**
```java 
class ExceptionDemo {
    public static void main(String[] args) {
        try {
            int a = 10 / 0;
        } catch (ArithmeticException e) {
            System.out.println("Error: " + e);
        } finally {
            System.out.println("Finally block executed");
        }
    }
}
```
18. **WAP to create and use a user-defined exception.**
```java 
import java.util.Scanner;

class InvalidAgeException extends Exception {
    InvalidAgeException(String message) {
        super(message);
    }
}

class AgeValidation {
    static void checkAge(int age) throws InvalidAgeException {
        if (age < 0 || age > 150) {
            throw new InvalidAgeException("Age cannot be less than 0 or greater than 150");
        } else {
            System.out.println("Valid Age: " + age);
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter age: ");
        int age = sc.nextInt();

        try {
            checkAge(age);
        } catch (InvalidAgeException e) {
            System.out.println("Exception Caught: " + e.getMessage());
        }
    }
}

```
1.  **WAP that accepts an email address from the user and perform basic operations using String methods**
```java 
import java.util.Scanner;

class EmailStringDemo {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // 1. Creation of String
        System.out.print("Enter Email: ");
        String email = sc.nextLine();

        // 2. Display Original String
        System.out.println("Original Email: " + email);

        // 3. Changing Case
        System.out.println("Uppercase: " + email.toUpperCase());
        System.out.println("Lowercase: " + email.toLowerCase());

        // 4. Character Extraction (Username & Domain)
        int atIndex = email.indexOf('@');
        String username = email.substring(0, atIndex);
        String domain = email.substring(atIndex + 1);

        System.out.println("Username: " + username);
        System.out.println("Domain: " + domain);

        // 5. String Comparison
        System.out.print("Enter another email to compare: ");
        String email2 = sc.nextLine();

        if (email.equals(email2))
            System.out.println("Both emails are equal");
        else
            System.out.println("Emails are not equal");

        // 6. Searching String
        System.out.print("Enter substring to search: ");
        String search = sc.nextLine();

        if (email.contains(search))
            System.out.println("Substring found in email");
        else
            System.out.println("Substring not found");

        // 7. Modifying String
        String modifiedEmail = email.replace("@", " [at] ");
        System.out.println("Modified Email: " + modifiedEmail);
    }
}
```
1.  **WAP to demonstrate difference between `String` and `StringBuffer`.**
```java 
class StringDemo {
    public static void main(String[] args) {
        String s = "Hello";
        s.concat(" World");
        System.out.println("The modified string is " + s);

        StringBuffer sb = new StringBuffer("Hello");
        sb.append(" World");
        System.out.println("The modified string is " + sb);
    }
}
```

1.  **WAP to create a thread using Thread class and Runnable interface.**
```java 
class MyThreadOne extends Thread {
  public void run() {
    int i = 1;
    while(true) {
      System.out.println(i + " Thread");
      i++;
    }
  }
}

class MyThreadTwo implements Runnable {
  public void run() {
    int i = 1;
    while(true) {
      System.out.println(i + " Runnable");
      i++;
    }    
  }
}
public class ThreadRunnable {
  public static void main(String[] args) {
    MyThreadOne t1 = new MyThreadOne(); 
    t1.start();               

    MyThreadTwo m = new MyThreadTwo();          
    Thread t = new Thread(m); 
    t.start();                

    int j = 1;
    while(true) {
      System.out.println(j + " World"); // Main thread execution
      j++;
    }   
  }
}
```

1.  **WAP to demonstrate synchronization in multithreading.**
```java 
class ATM
{    
  public void checkBalance(String name)
  {
    System.out.print(name + " Checking ");
    
    try{
      Thread.sleep(1000);
    }catch(Exception e) {}
    
    System.out.println("Balance");
  }
  
  public void withdraw(String name,int amount)
  {
    System.out.print(name + " withdrawing "); 
    
    try{
      Thread.sleep(1000);
    } catch(Exception e) {}
    
    System.out.println(amount);      
  }
}

class Customer extends Thread
{
  String name;
  int amount;
  ATM atm;
  
  Customer(String n,ATM a,int amt)
  {
    name=n;
    atm=a;
    amount=amt;
  }
  public void useATM()
  { 
    atm.checkBalance(name);
    atm.withdraw(name, amount);
  }
  public void run()
  {
    useATM();
  }
}

public class TestThread 
{
  public static void main(String[] args) 
  {
    ATM atm=new ATM(); //Shared Object
    Customer c1=new Customer("Smith",atm,100);
    Customer c2=new Customer("John",atm,200);
    c1.start();
    c2.start();     
  }   
}
```
23. **WAP to read data from a file and write it to another file.**
```java 
import java.io.*;

class FileCopy {
    public static void main(String[] args) throws Exception {
        FileInputStream in = new FileInputStream("input.txt");
        FileOutputStream out = new FileOutputStream("output.txt");

        int byteData;
        while ((byteData = in.read()) != -1)
            out.write(byteData);

        in.close();
        out.close();
    }
}
```
24. **WAP to store and sort elements using ArrayList and display using Iterator.**
```java 
import java.util.*;

class CollectionDemo {
    public static void main(String[] args) {
        ArrayList<Integer> list = new ArrayList<>();
        list.add(3);
        list.add(1);
        list.add(2);

        Collections.sort(list);
        Iterator iterator = list.iterator();
        while(iterator.hasNext())
        {
            System.out.print(iterator.next());
            System.out.print(" ");
        }
    }
}
```
25. **WAP to create a simple Swing-based GUI using JFrame and JButton with event handling.**
```java 

```
