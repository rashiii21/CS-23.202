[Program 1 : Create a class with four methods - Addition, Subtraction, Multiplication, Division.
Now, test all four methods in public static void main.](#Program1)

## Program1
```
class Calculator {

    int add(int a, int b) {
        return a + b;
    }

    int sub(int a, int b) {
        return a - b;
    }

    int mul(int a, int b) {
        return a * b;
    }

    double div(int a, int b) {
        if (b == 0) {
            System.out.println("Cannot divide by zero");
            return 0;
        }
        return (double) a / b;
    }

    public static void main(String[] args) {
        Calculator calc = new Calculator();

        int x = 10, y = 5;

        System.out.println("Addition: " + calc.add(x, y));
        System.out.println("Subtraction: " + calc.sub(x, y));
        System.out.println("Multiplication: " + calc.mul(x, y));
        System.out.println("Division: " + calc.div(x, y));
    }
}
```

<img width="338" height="177" alt="image" src="https://github.com/user-attachments/assets/483771ac-eb50-40d1-bea8-63c84051aef9" />

```

class LoopTest {
    public static void main(String[] args) {

        System.out.println("Using for loop:");
        for (int i = 1; i <= 5; i++) {
            System.out.println(i);
        }

        System.out.println("\nUsing while loop:");
        int j = 1;
        while (j <= 5) {
            System.out.println(j);
            j++;
        }

        System.out.println("\nUsing do-while loop:");
        int k = 1;
        do {
            System.out.println(k);
            k++;
        } while (k <= 5);
    }
}
```

<img width="375" height="561" alt="image" src="https://github.com/user-attachments/assets/ed7bff77-d529-4bfe-bdd8-c765e47501e0" />

```


import java.util.Scanner;

class GradeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter marks: ");
        int marks = sc.nextInt();

        if (marks >= 90) {
            System.out.println("Grade: A");
        } else if (marks >= 75) {
            System.out.println("Grade: B");
        } else if (marks >= 60) {
            System.out.println("Grade: C");
        } else if (marks >= 50) {
            System.out.println("Grade: D");
        } else {
            System.out.println("Grade: F");
        }

        sc.close();
    }
}
```

<img width="317" height="171" alt="image" src="https://github.com/user-attachments/assets/1a6e9383-c9b5-48e4-a041-8a3023adab87" />

```
import java.util.Scanner;

class SquareStars {

    int width, height;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter width: ");
        width = sc.nextInt();
        System.out.print("Enter height: ");
        height = sc.nextInt();
    }

    void printSquare() {
        for (int i = 1; i <= height; i++) {
            for (int j = 1; j <= width; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        SquareStars obj = new SquareStars();
        obj.input();
        obj.printSquare();
    }
}
```

<img width="312" height="383" alt="image" src="https://github.com/user-attachments/assets/4b8d5cb9-f32f-4abd-945a-f3f45c226467" />

```
import java.util.Scanner;

class PyramidStars {

    int n;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of rows: ");
        n = sc.nextInt();
    }

    void printPyramid() {
        for (int i = 1; i <= n; i++) {

            for (int j = 1; j <= n - i; j++) {
                System.out.print(" ");
            }

            for (int k = 1; k <= (2 * i - 1); k++) {
                System.out.print("*");
            }

            System.out.println();
        }
    }

    public static void main(String[] args) {
        PyramidStars obj = new PyramidStars();
        obj.input();
        obj.printPyramid();
    }
}
```

<img width="318" height="236" alt="image" src="https://github.com/user-attachments/assets/93cb5c24-f2a3-425d-b211-591993996cf2" />

```
import java.util.Scanner;

class Distance {
    int meters;
    int centimeters;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter meters: ");
        meters = sc.nextInt();
        System.out.print("Enter centimeters: ");
        centimeters = sc.nextInt();
    }

    Distance add(Distance d) {
        Distance sum = new Distance();
        sum.centimeters = this.centimeters + d.centimeters;
        sum.meters = this.meters + d.meters + sum.centimeters / 100;
        sum.centimeters = sum.centimeters % 100;  
        return sum;
    }

    void display() {
        System.out.println("Distance = " + meters + " meters and " + centimeters + " centimeters");
    }

    public static void main(String[] args) {
        Distance d1 = new Distance();
        Distance d2 = new Distance();

        System.out.println("Enter first distance:");
        d1.input();

        System.out.println("Enter second distance:");
        d2.input();

        Distance sum = d1.add(d2);

        System.out.print("Sum of distances: ");
        sum.display();
    }
}
```

<img width="519" height="253" alt="image" src="https://github.com/user-attachments/assets/0059438c-6c95-455b-8182-2986af72bb90" />

```
import java.util.Scanner;

class Distance {
    int meters;
    int centimeters;
    int millimeters;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter meters: ");
        meters = sc.nextInt();
        System.out.print("Enter centimeters: ");
        centimeters = sc.nextInt();
        System.out.print("Enter millimeters: ");
        millimeters = sc.nextInt();
    }

    Distance add(Distance d) {
        Distance sum = new Distance();

        sum.millimeters = this.millimeters + d.millimeters;
        sum.centimeters = this.centimeters + d.centimeters + sum.millimeters / 10; // 10 mm = 1 cm
        sum.millimeters = sum.millimeters % 10;

        sum.meters = this.meters + d.meters + sum.centimeters / 100; // 100 cm = 1 m
        sum.centimeters = sum.centimeters % 100;

        return sum;
    }

    void display() {
        System.out.println("Distance = " + meters + " meters, " + centimeters + " centimeters, and " + millimeters + " millimeters");
    }

    public static void main(String[] args) {
        Distance d1 = new Distance();
        Distance d2 = new Distance();

        System.out.println("Enter first distance:");
        d1.input();

        System.out.println("Enter second distance:");
        d2.input();

        Distance sum = d1.add(d2);

        System.out.print("Sum of distances: ");
        sum.display();
    }
}
```

<img width="526" height="325" alt="image" src="https://github.com/user-attachments/assets/da13122a-6a6a-4c7c-9152-98ea1afae6ce" />

```
import java.util.Scanner;

class Time {
    int hours;
    int minutes;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter hours: ");
        hours = sc.nextInt();
        System.out.print("Enter minutes: ");
        minutes = sc.nextInt();
    }

    Time add(Time t) {
        Time sum = new Time();
        sum.minutes = this.minutes + t.minutes;
        sum.hours = this.hours + t.hours + sum.minutes / 60; // 60 min = 1 hr
        sum.minutes = sum.minutes % 60;
        return sum;
    }

    void display() {
        System.out.println("Time = " + hours + " hours and " + minutes + " minutes");
    }

    public static void main(String[] args) {
        Time t1 = new Time();
        Time t2 = new Time();

        System.out.println("Enter first time:");
        t1.input();

        System.out.println("Enter second time:");
        t2.input();

        Time sum = t1.add(t2);

        System.out.print("Sum of times: ");
        sum.display();
    }
}
```

<img width="421" height="286" alt="image" src="https://github.com/user-attachments/assets/7eea1f29-1c49-4b34-8156-10a520f18a78" />

```
import java.util.Scanner;

class Time {
    int hours;
    int minutes;
    int seconds;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter hours: ");
        hours = sc.nextInt();
        System.out.print("Enter minutes: ");
        minutes = sc.nextInt();
        System.out.print("Enter seconds: ");
        seconds = sc.nextInt();
    }

    Time add(Time t) {
        Time sum = new Time();

        sum.seconds = this.seconds + t.seconds;
        sum.minutes = this.minutes + t.minutes + sum.seconds / 60;
        sum.seconds = sum.seconds % 60;

        sum.hours = this.hours + t.hours + sum.minutes / 60;
        sum.minutes = sum.minutes % 60;

        return sum;
    }

    void display() {
        System.out.println("Time = " + hours + " hours, " + minutes + " minutes, " + seconds + " seconds");
    }

    public static void main(String[] args) {
        Time t1 = new Time();
        Time t2 = new Time();

        System.out.println("Enter first time:");
        t1.input();

        System.out.println("Enter second time:");
        t2.input();

        Time sum = t1.add(t2);

        System.out.print("Sum of times: ");
        sum.display();
    }
}
```

<img width="513" height="307" alt="image" src="https://github.com/user-attachments/assets/9f5d61e8-7f95-46e7-b5a9-06e6ad60202e" />

```
import java.util.Scanner;

class OneDArray {
    int arr[];
    int n;

    // Input method
    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter size of array: ");
        n = sc.nextInt();

        arr = new int[n];
        System.out.println("Enter elements:");

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
    }

    // Output1: Print normally
    void output1() {
        System.out.println("Array elements:");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    // Output2: Print even elements
    void output2() {
        System.out.println("Even elements:");
        for (int i = 0; i < n; i++) {
            if (arr[i] % 2 == 0) {
                System.out.print(arr[i] + " ");
            }
        }
        System.out.println();
    }

    // Reverse method
    void reverse() {
        System.out.println("Reversed array:");
        for (int i = n - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    // Main method
    public static void main(String[] args) {
        OneDArray obj = new OneDArray();
        obj.input();
        obj.output1();
        obj.output2();
        obj.reverse();
    }
}
```
<img width="429" height="320" alt="image" src="https://github.com/user-attachments/assets/46644926-4dd2-4d61-a70a-6876434b58fb" />

```
import java.util.Scanner;

class MatrixOperations {
    int a[][], b[][];
    int r, c;

    // Input matrices
    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter rows and columns: ");
        r = sc.nextInt();
        c = sc.nextInt();

        a = new int[r][c];
        b = new int[r][c];

        System.out.println("Enter first matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                a[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter second matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                b[i][j] = sc.nextInt();
            }
        }
    }

    // Addition
    void addition() {
        System.out.println("Matrix Addition:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                System.out.print((a[i][j] + b[i][j]) + " ");
            }
            System.out.println();
        }
    }

    // Transpose of first matrix
    void transpose() {
        System.out.println("Transpose of first matrix:");
        for (int i = 0; i < c; i++) {
            for (int j = 0; j < r; j++) {
                System.out.print(a[j][i] + " ");
            }
            System.out.println();
        }
    }

    // Sum of rows
    void sumRows() {
        System.out.println("Sum of rows:");
        for (int i = 0; i < r; i++) {
            int sum = 0;
            for (int j = 0; j < c; j++) {
                sum += a[i][j];
            }
            System.out.println("Row " + i + ": " + sum);
        }
    }

    // Sum of columns
    void sumColumns() {
        System.out.println("Sum of columns:");
        for (int j = 0; j < c; j++) {
            int sum = 0;
            for (int i = 0; i < r; i++) {
                sum += a[i][j];
            }
            System.out.println("Column " + j + ": " + sum);
        }
    }

    // Sum of diagonal
    void sumDiagonal() {
        int sum = 0;
        for (int i = 0; i < r; i++) {
            sum += a[i][i]; // main diagonal
        }
        System.out.println("Sum of diagonal: " + sum);
    }

    // Main method
    public static void main(String[] args) {
        MatrixOperations obj = new MatrixOperations();
        obj.input();
        obj.addition();
        obj.transpose();
        obj.sumRows();
        obj.sumColumns();
        obj.sumDiagonal();
    }
}

```
<img width="489" height="624" alt="image" src="https://github.com/user-attachments/assets/3cc112d5-027d-48f5-ba81-4296038f6c66" />
```
import java.util.Scanner;

class Factorial {
    public static void main(String[] args) {
        int n, fact = 1;

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        n = sc.nextInt();

        for (int i = 1; i <= n; i++) {
            fact *= i;
        }

        System.out.println("Factorial = " + fact);
    }
}
```
<img width="374" height="136" alt="image" src="https://github.com/user-attachments/assets/fd13a424-ace1-4121-806b-04a4c5a6b334" />
```
import java.util.Scanner;

class Armstrong {
    public static void main(String[] args) {
        int n, temp, rem, sum = 0;

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        n = sc.nextInt();

        temp = n;

        while (n > 0) {
            rem = n % 10;
            sum += rem * rem * rem;
            n = n / 10;
        }

        if (temp == sum)
            System.out.println("Armstrong Number");
        else
            System.out.println("Not an Armstrong Number");
    }
}
```

<img width="408" height="152" alt="image" src="https://github.com/user-attachments/assets/5581de92-4082-465c-be22-c0cbced22333" />

```
import java.util.Scanner;

class Palindrome {
    public static void main(String[] args) {
        int n, rev = 0, rem, temp;

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        n = sc.nextInt();

        temp = n;

        while (n > 0) {
            rem = n % 10;
            rev = rev * 10 + rem;
            n = n / 10;
        }

        if (temp == rev)
            System.out.println("Palindrome Number");
        else
            System.out.println("Not a Palindrome Number");
    }
}

```

<img width="463" height="141" alt="image" src="https://github.com/user-attachments/assets/d2924a7e-9758-4123-ad7d-3baf239ff509" />

```
import java.util.Scanner;

class Fibonacci {
    public static void main(String[] args) {
        int n, a = 0, b = 1, c;

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of terms: ");
        n = sc.nextInt();

        System.out.println("Fibonacci Series:");
        System.out.print(a + " " + b + " ");

        for (int i = 3; i <= n; i++) {
            c = a + b;
            System.out.print(c + " ");
            a = b;
            b = c;
        }
    }
}
```

<img width="924" height="157" alt="image" src="https://github.com/user-attachments/assets/915217e5-358f-4d8e-9474-d8476acf0675" />
```
class Pattern {
    public static void main(String[] args) {

        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}

```
<img width="483" height="210" alt="image" src="https://github.com/user-attachments/assets/5f512385-dfa3-4dcd-b598-a7b701d3d4c2" />
```

