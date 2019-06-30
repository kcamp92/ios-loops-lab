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
let k = 1...150

for numbers in k {
print(numbers)
}
***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**
let a = 1..<150

for numbers in a {
print(numbers)
}
***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**
let cats = 15...80

for numbers in cats where numbers % 2 == 0{
print(numbers)
}
***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**
let dogs = 19...51

for numbers in dogs where numbers % 2 != 0{
print(numbers)
}
***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**
let rodents = 1..<100

for numbers in rodents where numbers % 5 == 0{
print(numbers)
}
***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**
let range = 1...40
let maxNumber = 40
var initialNumber = 7

for _ in range where initialNumber < maxNumber {
initialNumber += 10
print(initialNumber)
}
***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`
let amphibians = 20...150

for numbers in amphibians where numbers % 3 == 0{
print(numbers)
}

***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`


let amphibians = 20...150

for numbers in amphibians where numbers % 3 == 0 && numbers % 2 == 0 {
print(numbers)
}
***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

let range = 20...150
let maxNumber = 140
var initialNumber = 24

for _ in range where initialNumber < maxNumber {
initialNumber += 10
print(initialNumber)
}
***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

let range = 20...150

for value in range {
if value  == 31 {
print (value)
}
if value == 35 {
print (value)
}
if (value >= 40) && (value <= 60 ){
print (value)
}
}

***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// Your explanation here
```
It will run an infinite amount of times, because it is always true.
***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
var i = 5

while (i < 9) {
i += 1
print(i)
}
***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
var i = 5

while (i < 1005) {
i += 1
print(i)
}
***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 3) {
    i += 1
}
```

var i = 5

while (i < 1005 ) {
i += 1
if i <= 1003 {
print(i)

} else if i >= 1003 && i % 2 == 0 {
print(i)
} else {
print("")
}
}
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
```
No, there outputs will not be different, as theyre essentially asking the same thing, however the difference between the syntax is that "while" evaluates its condition at the start of each pass through the loop, and 
"repeat-while" evaluates its condition at the end of each pass through the loop.
***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

A break is a statment that is used to end the execution of a loop and/or a switch statement immediately, where as a continue statement tells a loop to stop what it is doing and jump to the start of the next iteration of the loop.
 
 Examples
 
 Break:
 
 let a = 0
 switch a {
 case 0:
 break;
 case 1:
 print("Good morning")
 case 2:
 print("Good afternoon")
 default:
 print("Good night");
 }
 print("Done")
 
 Continue:
 
 for i in 1...5 {
 for k in 1...4 {
 if k == 2 {
 continue
 }
 print("\(i) * \(k) = \(i * k)")
 }
 }
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
```

[]1 *
[]2 *
[]3 *
[]4
[]5
[]6
[]7
[]8 *
[]9 *
[]10 *

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
```

[]1 *
[]2 *
[]3 *
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

```
x = 1, y = 1
x = 2, y = 1
x = 3, y = 1
 
 It ends up printing only the 1 values for Y since the continue statment told it to stop what its doing for Y once it equals 2, and then proceed to continue the outerloop for all the X values.
***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.

for x in 0...10 {
for y in 0...10 {
print("\(x),\(y)", separator:
"", terminator:" ")
}
print("")
}

***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

for x in 0...10 {
for y in 0...10  where x-y >= 5 {
print("\(x),\(y)", separator:
"", terminator:" ")
}
print("")
}

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
var N = 5

for n in 1...5 {
print (n * n)
}

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

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

var n = 4
for n in 1...4
{ for n in 1...4
{ print ("*" , terminator: "")

}; print("")

}
***
