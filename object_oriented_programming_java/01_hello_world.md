# Hello World for java

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
```java
package moe.hello.hello;
import java.util.Scanner;
public class NewClass {
    public static void main(String[] args) {
        double water, init_temp, final_temp, energy;
        //water = init_temp = final_temp = energy = 0.0;
        Scanner sc = new Scanner(System.in);
        System.out.printf("%s", "input water in kg: ");
        water = sc.nextDouble();
        System.out.printf("%s", "input init temperature: ");
        init_temp = sc.nextDouble();
        System.out.printf("%s", "input final temperature: ");
        final_temp = sc.nextDouble();
        energy = water * (final_temp - init_temp) * 4184;
        System.out.printf("Energy: %.2f", energy);
    }
}

```
```java
package moe.hello.hello;
import javax.swing.*;
public class x {
    public static void main(String[] args) {
        String input = JOptionPane.showInputDialog("Input 3 digit number: ");
        int a = Integer.parseInt(input);
        if (a > 999 || a < 0) {
            JOptionPane.showMessageDialog(null,"Invalid input");
            System.exit(1);
        }
        int ret = (a / 100) * ((a % 100) / 10) * (a % 10);
        JOptionPane.showMessageDialog(null,"Result: "+ ret);
    }
}

```
Sleepy..........
I'm sleepy for java!!!!!!!!!
I need rust, though I'm C guy QwQ
# Mathmatical operations
Same as C, nothing to note........
Sleepy QwQ
# Type casting:
## Implicit type casting
double > float > long > int > char > short > byte
This is also called type widening, which is always safe.
## Explicit type casting
int a = (int)3.0; // a = 3 (Type narrowing)
int i = (int)3.9; // i = 3 (Truncation)
Type narrowing may cause truncation or overflow, this is not always safe.