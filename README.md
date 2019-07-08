# Arrays lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1

Create an array of strings called `colors` that contain "orange", "red", "yellow", "turquoise", and "lavender".

Then, using array subscripting and string interpolation, print out the String `"orange, yellow, and lavender are some of my favorite colors"`.

```
swift
//Q1
var colors = ["orange","red","yellow","turquoise","lavender"]

print("\(colors[0]), \(colors[2]), and \(colors[4]) are some of my favorite colors")
```

## Question 2

Remove "Illinois" and "Kansas" from the array below.

`var westernStates = ["California", "Oregon", "Washington", "Idaho", "Illinois", "Kansas"]`

```
swift
//Q2
var westernStates = ["California", "Oregon", "Washington", "Idaho", "Illinois", "Kansas"]

westernStates.remove(at: 4)
westernStates.remove(at: westernStates.count-1)
```


## Question 3

Iterate through the array below. For each state, print out the name of the state, a colon, and whether it is or is not **in the continental United States.**

`let moreStates = ["Hawaii", "New Mexico", "Alaska", "Montana", "Texas", "New York", "Florida"]`

```
swift
//Q3
let moreStates = ["Hawaii", "New Mexico", "Alaska", "Montana", "Texas", "New York", "Florida"]

for state in moreStates{
    if(state == "Hawaii"){
        print("\(state) is not in the continential United States")}
    else{
        print("\(state) is in the continential United States")
    }
}
```

## Question 4

Print out how many non-whitespace characters are in `myString`:

`let myString = "This is good practice with Strings!"`

Iterate through the array below. For each sentence, print out how many non-whitespace characters are in it.

`let myFavoriteQuotes = ["To be or not to be, that is the question.", "The only source of knowledge is experience.", "Mr. Gorbachev, tear down this wall!", "Four score and twenty years ago..."]`

```
swift
//Q4
let myFavoriteQuotes = ["To be or not to be, that is the question.", "The only source of knowledge is experience.", "Mr. Gorbachev, tear down this wall!", "Four score and twenty years ago..."]

var counter = 0

for i in myFavoriteQuotes{
    for j in i{
        if j != " "{counter+=1}
    }
}
print(counter)
```




## Question 5

Iterate through `garden` and place any 🌷 that you find into the `basket`. Replace any 🌷 that you pick up with `"dirt"`. Then print how many 🌷 are in your `basket`.

```swift
var garden = ["dirt","🌷","dirt","🌷","dirt","dirt","🌷","dirt","🌷","dirt"]
var basket = [String]()
```
```
swift
//Q5
var index = 0
var garden = ["dirt","🌷","dirt","🌷","dirt","dirt","🌷","dirt","🌷","dirt"]
var basket = [String]()

for i in garden{
    if i == "\u{1F337}"{
        basket.append("\u{1F337}")
        garden[index] = "dirt"
    }
    index += 1
}
print(garden)
```

## Question 6

The below array represents an unfinished batting lineup for a baseball team. **You, the coach,** need to make some last minute changes:

- Add "Suzuki" to the end of your lineup.
- Change "Jeter" to "Tejada".
- Change "Thomas" for "Guerrero"
- Put "Reyes" to bat 8th instead.

`var battingLineup = ["Reyes", "Jeter", "Ramirez", "Pujols","Griffey","Thomas","Jones", "Rodriguez"]`

```
var battingLineup = ["Reyes", "Jeter", "Ramirez", "Pujols","Griffey","Thomas","Jones", "Rodriguez"]

battingLineup.append("Suzuki")
battingLineup[1] = "Tejada"
battingLineup[5] = "Guerrero"
battingLineup.remove(at: 0)
battingLineup.append("Reyes")
```


## Question 7

Given an array of Ints, find out if it contains a target number.  

(The built-in `contains(_:)` function will do this, but you aren't allowed to use it for this exercise.)


```swift
var numbers: [Int]

let target: Int = 32
```

Ex.1

```swift
numbers = [4,2,6,73,32,4,2,1]

target = 32

//true
```



Ex. 2

```swift
numbers = [32459,2,4,5,1,4,2,1]

target = 3

//false
```
```
//Q7
var target = 32
var answer: Bool = false


for num in numbers{
    if num == target{
        answer = true
        break        
    }else{
        answer = false
    }
}

print(answer)
```


## Question 8

Find the largest value in an array of Int.  Do not use the built-in `max()` method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

//This creates an array of 100 numbers in between 0 and 200.  For now, you don't need to worry about how it does that.
```
```
swift
//Q8 Solution
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

let newArray = arrayOfNumbers.sorted()
print(newArray[newArray.count-1])

```


## Question 9

Find the smallest value in an array of Int.  Do not use the built in min() method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

//This creates an array of 100 numbers in between 0 and 200.  For now, you don't need to worry about how it does that.
```
```
swift
//Q9
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

let newArray = arrayOfNumbers.sorted()
print(newArray[0])

```


## Question 10

Iterate through `secondListOfNumbers`, and print out all the odd numbers.

`var secondListOfNumbers = [19,13,14,19,101,10000,141,404]`

```
swift
//Q10
var secondListOfNumbers = [19,13,14,19,101,10000,141,404]

for i in secondListOfNumbers where i % 2 != 0 {print(i, separator: "", terminator: " ")}
```


## Question 11

Iterate through `thirdListOfNumbers`, and print out the sum.

`var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]`

```
swift
//Q11
var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]
var sum = 0

for i in thirdListOfNumbers{sum += i}; print(sum)

```


## Question 12

Iterate through `thirdListOfNumbers`, and print out the sum of all the even numbers.

`var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]`
```
swift
//Q12
var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]
var evenSum = 0

for i in thirdListOfNumbers where i % 2 == 0{evenSum += i};print(evenSum)
```


## Question 13

Append every Int that appears in both `listOne` and `listTwo` to the `sharedElements` array. Then print **how many Ints** are shared.

```swift
var listOne = [28, 64, 7, 96, 13, 32, 94, 11, 80, 68]
var listTwo = [18, 94, 48, 6, 42, 68, 79, 76, 13, 7]
var sharedElements = [Int]()
```
```
//Q13
var listOne = [28, 64, 7, 96, 13, 32, 94, 11, 80, 68]
var listTwo = [18, 94, 48, 6, 42, 68, 79, 76, 13, 7]
var sharedElements = [Int]()

for i in listOne{
if listTwo.contains(i){
sharedElements.append(i)}
}

for j in sharedElements{print(j, separator: "", terminator: " ")}

```


## Question 14

Write code such that `noDupeList` has all the same Ints as `dupeFriendlyList`, but has no more than one of each Int.

```swift
var dupeFriendlyList = [4,2,6,2,2,6,4,9,2,1]
var noDupeList: [Int] = []
```
```
swift
//Q14
var dupeFriendlyList = [4,2,6,2,2,6,4,9,2,1]
var noDupeList: [Int] = []

for i in dupeFriendlyList{
if !(noDupeList.contains(i)){noDupeList.append(i)}
}

for j in noDupeList {print(j, separator: "", terminator: " ")}

```


## Question 15

Find the second smallest number in an Array of Ints

`let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}`

```
swift
//Q15
let arrayOfNumbers: [Int] = (1...10).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

var sortedArrayOfNumbers = arrayOfNumbers.sorted()

var secondSmallest = sortedArrayOfNumbers[0]

for i in sortedArrayOfNumbers{
if(secondSmallest > i){ secondSmallest = i}
}; print(secondSmallest)
```

## Question 16

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Find the sum of all the multiples of 3 or 5 below 1000.
```
swift
let range = 0...1000
var sum = 0

for i in range where i % 3 == 0 || i % 5 == 0{
sum += i
}; print(sum)
```


## Question 17

Make an array that contains all elements that appear **more than twice** in `someRepeatsAgain`.

```swift
var someRepeatsAgain = [25,11,30,31,50,28,4,37,13,20,24,38,28,14,44,33,7,43,39,35,36,42,1,40,7,14,23,46,21,39,11,42,12,38,41,48,20,23,29,24,50,41,38,23,11,30,50,13,13,16,10,8,3,43,10,20,28,39,24,36,21,13,40,25,37,39,31,4,46,20,38,2,7,11,11,41,45,9,49,31,38,23,41,16,49,29,14,6,6,11,5,39,13,17,43,1,1,15,25]
```
```
swift
//Q17
var someRepeatsAgain = [25,11,30,31,50,28,4,37,13,20,24,38,28,14,44,33,7,43,39,35,36,42,1,40,7,14,23,46,21,39,11,42,12,38,41,48,20,23,29,24,50,41,38,23,11,30,50,13,13,16,10,8,3,43,10,20,28,39,24,36,21,13,40,25,37,39,31,4,46,20,38,2,7,11,11,41,45,9,49,31,38,23,41,16,49,29,14,6,6,11,5,39,13,17,43,1,1,15,25]

let mappedItems = someRepeatsAgain.map {($0,1)}
let counts = Dictionary(mappedItems, uniquingKeysWith: +)
var emptyArray: [Int] = []

for i in counts {
if (i.value > 2){emptyArray.append(i.key)}
}

for num in emptyArray{print(num, separator: "", terminator: " ")}
```


## Question 18

Identify if there are 3 integers that sum to 10 in the following array. If so, print them as a triplet. If there are multiple triplets, print all possible triplets.

`var tripleSumArr = [-20,-14, -8,-5,-3,-2,1,2,3,4,9,15,20,30]`

```
var tripleSumArr = [-20,-14, -8,-5,-3,-2,1,2,3,4,9,15,20,30]
tripleSumArr.sort()

var sum = 10

//use 3 nested for loops to generate all possible triplets
//compare the sum of all possible triplets

for i in 0..<tripleSumArr.count - 2{
    for j in 1+i..<tripleSumArr.count - 1{
        for k in 2+j..<tripleSumArr.count{
            if (tripleSumArr[i] + tripleSumArr[j] + tripleSumArr[k]) == sum{
            print("Triplets are \(tripleSumArr[i]),\(tripleSumArr[j]),\(tripleSumArr[k])")
            }
        }
    }
}
```

## Question 19

Given an array of Strings, find the the String with the most "a"s in it.

input: `["apes", "abba", "apple"]`

output: `"abba"`


## Question 20

Given an Array of Arrays of Ints, find the Array of Ints with the largest sum:

Input: `[[2,4,1],[3,0],[9,3]]`

Output: `[9,3]`

```
swift
//Q20

var input = [[2,4,1],[3,0],[9,3]]
var indexOfAnswer = 0
var counter = 0
var largestSum = 0

//output = [9,3]

for i in input{
var sum = 0

for j in i{ sum += j }
    if sum > largestSum {
        largestSum = sum
        indexOfAnswer = counter
    }
    counter += 1
}; print(input[indexOfAnswer])

```


## Question 21

Given an Array of Tuples of type `(Int, Int)`, create an array containing all the tuples where the first Int is equal to the second Int.

Input: `[(4,2), (-3,-3), (1,1), (3,9)]`

Output: `[(-3,-3), (1,1)]`

```
var input = [(4,2), (-3,-3), (1,1), (3,9)]
var output: [(Int,Int)] = []

for i in input{
    if(i.0 == i.1){output.append(i)}
}
print(output)
```


## Question 22

Given an Array of Bools, make a variable called `allAreTrue` that is true if all of the Bools are true and false if any of them are false.

Input: `[true, false, true, true]`

Output: `false`

```
swift
//22
var input: [Bool] = [true, false, true, true]
var allAreTrue : Bool = true


for i in input{
    if(i == false) {allAreTrue = false}
}
print(allAreTrue)
```



## Question 23

Given an Array of Ranges of Ints, create an array that has all the values from all the ranges in order from smallest to greatest with no duplicates.

Input: `[0..<3 , 2..<10, -4..<6, 13..<14]`

Output: `[-4,-3,-2,-1,0,1,2,3,4,5,6,7,8,9,10,13]`


## Question 24

Given an array of Characters, create a String ignoring and uppercase Characters and spaces.  Then uppercase every other character of the String.

Input: `let arr: [Character] = ["a", "p","P","l","E"," ","S","a","u","C,"e"]`

Output: `"ApLeAuE"`

```
swift
//Q24
let arr: [Character] = ["a", "p","P","l","E"," ","S","a","u","C","e"]
var output = String()
var index = 0
for c in arr{
    if index % 2 == 0{
    output.append(c.uppercased())
}else{
    output.append(c.lowercased())
}
index += 1
}; print(output)
```


## Question 25

Print out each element in `myMatrix`

`var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]`

```
swift
//Q25

var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]

for i in myMatrix{ print(i) }
```

## Question 26

Print out the sum of the diagonals of `myMatrix`.

`var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]`

```
swift
var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]
//var myMatrix = [[1,2,3], [4,5,6], [7,8,9]]

let numOfRows = myMatrix.count
var counter = 0 //to keep track on how many diagonals there are.  For debugging purposes. Not needed otherwise

for r in 0...numOfRows-1{
    var row = r, col = 0, sum = 0

    while row >= 0 {
        sum += myMatrix[row][col]
        row -= 1
        col += 1
    }
    counter += 1
    print("Diagonal \(counter): \(sum)")
}

let numOfCol = 3

for c in 1...numOfCol-1{
    var row = numOfRows-1, col = c, sum = 0

    while(col <= numOfCol-1){
        sum += myMatrix[row][col]
        row -= 1
        col += 1
    }
    counter += 1
    print("Diagonal \(counter): \(sum)")
}

```




## Question 27

Using for loops, rotate `matrixToRotate` 90 degrees.

var matrixToRotate = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

![Matrix Rotation](images/rotated_matrix.jpeg)

```
swift
//Q27

var matrixToRotate = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

var n = 3

for i in 0..<n/2 {
    for j in i..<n-i-1{
        let temp = matrixToRotate[i][j]
        matrixToRotate[i][j] = matrixToRotate[n-1-j][i]
        matrixToRotate[n-1-j][i] = matrixToRotate[n-1-i][n-1-j]
        matrixToRotate[n-1-i][n-1-j] = matrixToRotate[j][n-1-i]
        matrixToRotate[j][n-1-i] = temp
    }
}

for i in 0..<n {
    for j in 0..<n{
        print(matrixToRotate[i][j], separator: "", terminator: " ")
    }
    print("")
}

```
