# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**
```swift
let range = 1...150

for i in range {
    print(i)
}
```
***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**
```swift
let range = 142..<159

for i in range {
    print(i)
}
```
***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**
```swift
let range3 = 15...80

for evenNumber in range3 where evenNumber % 2 == 0 {
    print(evenNumber)
}
```
***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**
```swift
let range4 = 19...51

for oddNumber in range4 where oddNumber % 2 != 0 {
    print(oddNumber)
}

```
***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

```swift
let range5 = 1...100

for endsInFive in range5 where endsInFive % 10 == 5 {
    print(endsInFive)
}
```
***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**
```swift
let range6 = 1...40

for endsInSeven in range6 where endsInSeven % 10 == 7 {
    print(endsInSeven)
}
```
***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

```swift
let range7 = 20...150

for divisibleByThree in range7 where divisibleByThree % 3 == 0 {
    print(divisibleByThree)
}
```

***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`
```swift
let range8 = 20...150

for divisibleByTwoAndThree in range8 where divisibleByTwoAndThree % 2 == 0 && divisibleByTwoAndThree % 3 == 0 {
    print(divisibleByTwoAndThree)
}
```

***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

```swift
let range9 = 20...150

for endsInFour in range9 where endsInFour % 10 == 4 {
    print(endsInFour)
}
```
***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`
```swift
let range10 = 20...150

for num in range10 where num == 31 || num == 35 || (40...60).contains(num) {
    print(num)
}

```
***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// Your explanation here
The loop is infinite, condition states that while i is greater than 3 increment the variable by 1. i starts at 5 so it will always be greater than 3.
```

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i > 3) {
    i += 1
    if i == 9 {
        break
    }
}
```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5
var counter = 0

while (i > 3) {
    i += 1
    counter += 1
    if counter == 1000 {
        break
    }
}

```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5
var counter = 0

while (i > 3) {
    i += 1
    counter += 1
    if counter == 1000 {
        if i % 2 == 0 {
            print(i)
        }
        break
    }
}
```

***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10

//It repeats the operation print the string "i = current value of i" and increment last value of 1 by one while the value of i is less OR equal to 10. This loop runs 10 times.
```

***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

```swift

//`continue` ends current iteration of the loop if statement is true, but loop will run the upcoming applicable iterations until loop breaks, if breaks. `break` will break the loop and no other iterations will occur after.

for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}

//This prints 1, 2, 3, 8, 9, 10 because block only prints i when if statement above is not met.

for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}

//This loop breaks when i = four, i.e. when the conditional statement is met. It prints 1, 2, 3.
```
***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}
// This prints 1, 2, 3, 8, 9, 10 because block only prints i when if statement above is not met.
```

[x]1
[X]2
[X]3
[]4
[]5
[]6
[]7
[X]8
[X]9
[X]10

***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}

//This loop breaks when i = four, i.e. when the conditional statement is met. It prints 1, 2, 3.
```

[X]1
[X]2
[X]3
[]4
[]5
[]6
[]7
[]8
[]9
[]10

***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2{
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}

// This prints:
//x = 1, y = 1
//x = 2, y = 1
//x = 3, y = 1
// The block only prints ("x = \(x), y = \(y)") once per cycle because every time y == 2 in each `innerloop`, `continue` will kick out to `outerloop` and skip the printing.
```

***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.

```swift
for x in 0...10 {
    for y in 0...10  {
        print("(\(x),\(y))")
    }
}
```
***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

```swift
for x in 0...10 {
    for y in 0...10  {
        if x - y <= 5 {
            print("(\(x),\(y))")
        }
    }
}
```
***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25
```
```swift
for x in 1...N {
    print("\(x * x)")
}
```
***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```

```swift
for _ in 1...n {
    for _ in 1...n  {
        print("*", terminator:"")
    }
    print("")
}
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

***
