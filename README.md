# [go back Overview](https://github.com/c4arl0s)

# [ControlFlow - Content](https://github.com/c4arl0s/ControlFlow#go-back-overview)

1. [Logical Operators](https://github.com/c4arl0s/ControlFlow#1-logical-operators)
2. [If statements](https://github.com/c4arl0s/ControlFlow#2-if-statements)
3. [if-else Statements](https://github.com/c4arl0s/ControlFlow#3-if-else-statements)
4. [Boolean Values](https://github.com/c4arl0s/ControlFlow#4-boolean-values)
5. [Switch Statement](https://github.com/c4arl0s/ControlFlow#5-switch-statement)
6. [Ternary Operator](https://github.com/c4arl0s/ControlFlow#6-ternary-operator)

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
# 4. [Boolean Values](https://github.com/c4arl0s/ControlFlow#controlflow---content)
# 5. [Switch Statement](https://github.com/c4arl0s/ControlFlow#controlflow---content)
# 6. [Ternary Operator](https://github.com/c4arl0s/ControlFlow#controlflow---content)