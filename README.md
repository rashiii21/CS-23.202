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
