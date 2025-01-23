
# Loops (Flow Control) in Java

This README provides explanations and code examples for various loop concepts in Java.

## 1. Loops Basics
Loops are used to execute a block of code repeatedly based on a condition. Common loops in Java are:
- `while`
- `for`
- `do-while`

---

## 2. `while` Loop
Executes a block of code as long as the condition is `true`.

```java
public class WhileLoopExample {
    public static void main(String[] args) {
        int i = 1;
        while (i <= 5) {
            System.out.println("Count: " + i);
            i++;
        }
    }
}
```

---

## 3. Print Numbers from 1 to 10
Use a loop to print numbers from 1 to 10.

```java
public class PrintNumbers {
    public static void main(String[] args) {
        int i = 1;
        while (i <= 10) {
            System.out.println(i);
            i++;
        }
    }
}
```

---

## 4. Print Numbers from 1 to `n`
Print numbers up to a user-defined value `n`.

```java
import java.util.Scanner;

public class PrintNumbersToN {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the value of n: ");
        int n = sc.nextInt();
        
        for (int i = 1; i <= n; i++) {
            System.out.println(i);
        }
    }
}
```

---

## 5. Sum of First `N` Natural Numbers
Calculate the sum of the first `N` natural numbers.

```java
import java.util.Scanner;

public class SumOfNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the value of n: ");
        int n = sc.nextInt();
        int sum = 0;
        
        for (int i = 1; i <= n; i++) {
            sum += i;
        }
        
        System.out.println("Sum of first " + n + " natural numbers is: " + sum);
    }
}
```

---

## 6. `for` Loop
A concise loop that executes for a fixed number of iterations.

```java
public class ForLoopExample {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println("Iteration: " + i);
        }
    }
}
```

---

## 7. Print Square Pattern
Print a square pattern of stars (`*`).

```java
public class SquarePattern {
    public static void main(String[] args) {
        int n = 5;
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

---

## 8. Print Reverse of a Number
Print digits of a number in reverse order.

```java
import java.util.Scanner;

public class ReverseNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int num = sc.nextInt();
        
        while (num > 0) {
            int digit = num % 10;
            System.out.print(digit);
            num /= 10;
        }
    }
}
```

---

## 9. Reverse the Given Number
Reverse the given number completely.

```java
import java.util.Scanner;

public class ReverseNumberComplete {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int num = sc.nextInt();
        int reverse = 0;
        
        while (num > 0) {
            int digit = num % 10;
            reverse = reverse * 10 + digit;
            num /= 10;
        }
        
        System.out.println("Reversed number: " + reverse);
    }
}
```

---

## 10. `do-while` Loop
Executes at least once, then checks the condition.

```java
public class DoWhileExample {
    public static void main(String[] args) {
        int i = 1;
        do {
            System.out.println("Iteration: " + i);
            i++;
        } while (i <= 5);
    }
}
```

---

## 11. Break Statement
Stops a loop when the condition is met.

```java
public class BreakExample {
    public static void main(String[] args) {
        for (int i = 1; i <= 10; i++) {
            if (i == 5) {
                break; // Exit the loop
            }
            System.out.println(i);
        }
    }
}
```

---

## 12. Question - Break Keyword
Question: How does the `break` keyword work?
- **Answer**: It immediately exits the loop.

---

## 13. Continue Statement
Skips the current iteration and proceeds to the next.

```java
public class ContinueExample {
    public static void main(String[] args) {
        for (int i = 1; i <= 10; i++) {
            if (i % 2 == 0) {
                continue; // Skip even numbers
            }
            System.out.println(i);
        }
    }
}
```

---

## 14. Question - Continue Keyword
Question: What does the `continue` keyword do?
- **Answer**: It skips the current iteration and moves to the next one.

---

## 15. Check if a Number is Prime or Not
Determine if a number is prime.

```java
import java.util.Scanner;

public class PrimeNumberCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int num = sc.nextInt();
        boolean isPrime = true;
        
        if (num <= 1) {
            isPrime = false;
        } else {
            for (int i = 2; i <= Math.sqrt(num); i++) {
                if (num % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }
        
        if (isPrime) {
            System.out.println(num + " is a prime number.");
        } else {
            System.out.println(num + " is not a prime number.");
        }
    }
}
```

---

## 16. Practice Questions
Try these questions:
1. Print numbers from 10 to 1.
2. Print the multiplication table of a number.
3. Check if a number is Armstrong or not.

---

## 17. Solutions for Practice Questions
### 1. Print numbers from 10 to 1:
```java
for (int i = 10; i >= 1; i--) {
    System.out.println(i);
}
```

### 2. Print the multiplication table of a number:
```java
Scanner sc = new Scanner(System.in);
System.out.print("Enter a number: ");
int num = sc.nextInt();
for (int i = 1; i <= 10; i++) {
    System.out.println(num + " x " + i + " = " + (num * i));
}
```

### 3. Check if a number is Armstrong:
```java
Scanner sc = new Scanner(System.in);
System.out.print("Enter a number: ");
int num = sc.nextInt();
int original = num, sum = 0;
while (num > 0) {
    int digit = num % 10;
    sum += digit * digit * digit;
    num /= 10;
}
if (sum == original) {
    System.out.println(original + " is an Armstrong number.");
} else {
    System.out.println(original + " is not an Armstrong number.");
}
```
