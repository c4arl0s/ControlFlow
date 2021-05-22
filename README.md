# [go back Overview](https://github.com/c4arl0s/AppDevelopmentWithSwift#1-getting-started-with-app-development)

# [ControlFlow - Content](https://github.com/c4arl0s/ControlFlow#go-back-overview)

1. [x] [1. Logical Operators](https://github.com/c4arl0s/ControlFlow#1-logical-operators)
2. [x] [2. If statements](https://github.com/c4arl0s/ControlFlow#2-if-statements)
3. [x] [3. if-else Statements](https://github.com/c4arl0s/ControlFlow#3-if-else-statements)
4. [x] [4. Boolean Values](https://github.com/c4arl0s/ControlFlow#4-boolean-values)
5. [x] [5. Switch Statement](https://github.com/c4arl0s/ControlFlow#5-switch-statement)
6. [x] [6. Ternary Operator](https://github.com/c4arl0s/ControlFlow#6-ternary-operator)
 
# [ControlFlow](https://github.com/c4arl0s/ControlFlow#controlflow---content)

Think of an application you use that requires you to log in. If you launch the application and you are already logged in, the app displays your data. If you are not logged in, the app asks for your login credentials. If you enter a correct user name and password, you are logged in  and the app displays your data. If you enter incorrect credentials, you are asked to enter the correct information.

This example describes one common interaction that requires multiple checks and runs code based on the results.

**These checks are called conditional statements, and they are par of a broader concept called control flow**. As a developer, you have control flow tools that check for certain conditions and execute different blocks of code based on those conditions.

Based on the outcome of a set of conditions, you can use a variety of statements to control what code is executed. These conditional statements are all examples of control flow.

# 1. [Logical Operators](https://github.com/c4arl0s/ControlFlow#controlflow---content)

Each `if` statements uses a logical operator to decide if something is `true` or `false`. The result determines whether to run the block of code or to skip it.

Start by taking a look through this list of the most common logical operators.

![Screen Shot 2021-03-19 at 13 49 34](https://user-images.githubusercontent.com/24994818/111834971-f6732280-88b9-11eb-9b92-321743cf7f07.png)

You can mix and match logical operators to create what is called a Boolean value, or `Bool`. Boolean values are either `true` or `false` and can be combined with an `if` statement to determine if code should be run or skipped.

# 2. [If statements](https://github.com/c4arl0s/ControlFlow#controlflow---content)

The most straightforward conditional statement is the `if` statement. An `if` statement basically says "if this condition is true, then run this block of code". If the condition is not true, the program will skip the block of code.

In most cases, you will use an `if` statement to check simple conditions with only a few possible outcomes. Here is an example:

```swift
let temperature = 100
if temperature >= 100 {
    print("the water is boiling")
}
```

Console output:

```console
the water is boiling
```

The `temperature` constant is equal to `100` and the `if` statement prints text if `temperature` is greater than or equal to `100`. Because the `if` statement resolves to `true`, the block of code accompanying the `if` statement is executed.

# 3. [if-else Statements](https://github.com/c4arl0s/ControlFlow#controlflow---content)

You just learned that an `if` statements will run a block of code if the condition is true. But what if the condition is not true?. By adding an `else` clause to an `if` statement, you can specify a block of code to execute if the condition is not true.

```swift
let temperature = 100
if temperature >= 100 {
    print("The water is boiling.")
} else {
    print("The water is not boiling")
}
```

You can take this idea even further. By using `else if`, you can declare more blocks of code to run based on any number of conditions. The following code checks for the position of an athlete in a race and responds accordingly:

```swift
var finishPosition = 2
if finishPosition == 1 {
    print("Congratulations, you won the gold medal!")
} else if finishPosition == 2 {
    print("You came in second place, you won a silver medal!")
} else {
    print("You did not win a gold or silver medal.")
}
```

You can use many `else if` statements to account for any number of potential cases.

# 4. [Boolean Values](https://github.com/c4arl0s/ControlFlow#controlflow---content)

You can assign the results of a logical operator to a `Bool` constant or variable in order to check or access the value later. `Bool` values can only be `true` or `false`.

In the following code, the `Bool` statement determines that `number` does not qualify as `isSmallNumber`.

```swift
let number = 1000
let isSmallNumber = number < 10
// number is not less  than 10, so isSmallNumber is assigned a false value-
```

And here, the `bool` statement determines that `currentSpeed` does not qualify as `isSpeeding`.

```swift
let speedLimit = 65
let currentSpeed = 72
let isSpeeding = currentSpeed > speedLimit
// currentSpeed is greater than the speedLimit, so isSpeeding is assigned a true value.
```

It is also possible to invert a `Bool` value using the logical NOT operator, which is represented with `!`.

```swift
var isSnowing = false
if !isSnowing {
    print("It is not snowing.")
}
```

Console output:

```console
It is not snowing.
```

In the same way, you can use the logical AND operator, represented by `&&`, to check if two or more conditions are true.

```swift
let temperature = 100
if temperature >= 65 && temperature <= 75 {
    print("The temperature is just right.")
} else if temperature < 65 {
    print("It is too cold.")
} else {
    print("It is too hot.")
}
```

Console output:

```console
The temperature is just right.
```

In the above code, the temperature meets both conditions: It is greater than or equal to 65 degrees and less than or equal to 75 degrees. It is just right.

You have yet another option: the logical OR operator, presented by `||`, to check if either one of two conditions is true.

```swift
var isPluggedIn = false
var hasBatteryPower = true
if isPluggedIn || hasBatteryPower {
    print("You can use your laptop.")
} else {
    print("woow")
}
```

Console output:

```console
You can use your laptop.
```

# 5. [Switch Statement](https://github.com/c4arl0s/ControlFlow#controlflow---content)

You have seen `if` statements and `if-else` statements that allow you to run certain blocks of code depending on certain conditions. But a long chain of `if`, `else if`, `else if ... else` statements can become messy and hard to read after a small number of options. Swift gas another tool for control flow called a `switch` statement, which is great for working many potential conditions.

A basic `switch` statement takes a value with multiple options and allows you to run separate code based on each option, or `case`. You can also provide a `default` case to specify a block of code that will run in all the cases you have not specifically defined.

Consider the code that prints a name for a vehicle based on its number of wheels:

```swift
let numberOfWheels = 2
switch numberOfWheels {
case 1:
    print("Unicylce")
case 2:
    print("Bicycle")
case 3:
    print("Tricycle")
case 4:
    print("Quadcycle")
defualt:
    print("That is a lot of wheels!")
}
```

Given a constant `numberOfWheels`, the code provides a separate action if the value is 1, 2, 3, or 4. It also provides an action if `numberOfWheels`is anything else.

This code could be written as a nested `if-else` statement, but it would quickly become difficult to parse.

Any given `case` statement can also evaluate multiple conditions at once. The following code, for example, checks whether a character is a vowel or not:

```swift
let character = "z"
switch characther {
case "a", "e", "i", "o", "u" :
    print("This character is a vowel.")
default:
    print("This character is a constant.")
}
```

When working with numbers, you can use interval matching to check for inclusion in a range. Take a look at the syntax in the following code snippet:

```swift
switch distance {
case 0...9:
    print("Your destination is close.")
case 10...99:
    print("Your destination is a medium distance from here.")
case 100...999:
    print("Your destination is far from here.")
default:
    print("Are you sure you want to travel this far?.")
}

```

The `switch` operator is the right tool for control flow when you want to run different code based on many different conditions.

# 6. [Ternary Operator](https://github.com/c4arl0s/ControlFlow#controlflow---content)

An interesting (and very common) use case for an `if` statement is to set a variable or return a value. If a certain condition is `true`, you want to set a variable to one value. If the condition is `false`, you want to set the variable to a different value.

Consider the following code. It checks if the value of one number is greater than the other and assigns the higher value to a `largest` variable:

```swift
var largest: Int
let a = 15
let b = 4
if a > b {
    largest = a
} else {
    largest = b
}
```

Because this situation is so common in programming, many languages include a special operator, called a ternary operator (`?:`), for writing more concise code.

The ternary operator has three parts:

1. A question with a `true` or `false` answer.
2. A value if the answer to the question is `true`.
3. A value if the answer to the question is `false`.

here is an example:

```swift
var largest: Int
let a = 15
let b = 4
largest = a > b ? a : b
```

Take a close look at the last line of code. You can read it as: "If `a > b`, assign `a` to the `largest` constant, otherwise, assign `b`. In this case, `a` is greater than `b`, so it is assigned to `largest`.

Keep in mind that it is never required that you use the ternary operator in Swift. But it is very useful shorthand for assigning a value based on a condition, rather than resorting to a more complex `if-else` statement.

