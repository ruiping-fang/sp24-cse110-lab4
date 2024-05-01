- part2-question1

  - It will log `3`. `console.log(i);` is being called after the `for` loop has completed. Since `i` was declared with the `var` keyword, it is function-scoped, which means it is available throughout the entire `discountPrices` function, including after the `for` loop. Therefore, `console.log(i);` will log the value of `i` after the loop, which would be `3`

- part2-question2

  - The value `150 ` will be logged. Line 13 is being called outside of the `for` loop where `discountedPrice` is declared. The `var` keyword provides function scope for variables, not block scope. It's available throughout the entire `discountPrices` function. when `console.log(discountedPrice);` is called, it will log the last calculated `discountedPrice` to the console, which would be the discounted price of the last item in the prices array after the discount has been applied.

- part2-question3

  - It will log `150` on the console.The variable `finalPrice` is declared at the function scope using the `var` keyword, meaning it is accessible throughout the entire function. After the last iteration of the loop, `finalPrice` will hold the last computed value, which is `150`.

- part2-question4

  - The function `discountPrices` will return `[50, 100, 150]`. The `discountPrices` function will iterate over an array of prices and calculate a discounted price for each element. It will round the discounted price to two decimal places and then push that rounded price into the discounted array. After the loop completes for all items in the prices array, the function will return the discounted array.

- part2-question5

  - error. Because `i` is declared inside the scope, so it's not accessible outside of the scope.

- part2-question6

  - At line 13, `console.log(discountedPrice);` will cause a `ReferenceError` because `discountedPrice` is declared inside the `for` loop with `let`, which means it has block scope and is not accessible outside of the block in which it is defined. Since `console.log(discountedPrice);` is outside the `for` loop, the variable `discountedPrice` is not in scope there.

- part2-question7

  - It will log `150` to the console. There will be no error because `finalPrice` is declared with `let` at the function scope, not block scope, making it accessible throughout the entire function, including after the `for` loop.

  The output is `150` because it's the last value assigned to `finalPrice` in the loop for the array [100, 200, 300] with a 0.5 discount.

- part2-question8

  - The function will return an array `[50, 100, 150]`. It applies a 50% discount to each price in the input array `[100, 200, 300]` and rounds the result to the nearest whole number before returning it.

- part2-question9

  - It will throw a ReferenceError: i is not defined. Because `i` is defined within the for loop using `let` keyword, which means it has block scope and is not accessible outside of the block in which it is defined.

- part2-question10

  - At line 12 `console.log(length);` is called. This will not cause an error. And will log the length of the array, which is `3`.

  The variable `length` is defined within the `discountPrices` function with the `const` keyword, which means it has block scope and it's accessible throughout the entire function, including after the `for` loop. So when line 13 is executed, it will simply print the value of the `length` variable to the console

- part2-question11

  - The function `discountPrices` will return `discounted` array `[50, 100, 150]`. The `discountPrices` function will iterate over an array of prices and calculate a discounted price for each element and push discounted price into the `discounted` array. After the loop completes for all items in the prices array, the function will return the `discounted` array.

- part2-question12

  ```javascript
  student.name; //A
  student["Grad Year"]; //B
  student.greeting(); //C
  student["Favorite Teacher"].name; //D
  student.courseLoad[0]; //E
  ```

- part2-question13

  - Arithmetic

    A. ` '3' + 2`

    - output: `'32'`. The `+` operator is also the string concatenation operator. If one of the operands `'3'` is a string, JavaScript will convert the other operand to a string as well and concatenate them.

    B. `'3' - 2`

    - output: 1. The `-` operator is strictly for arithmetic and does not concatenate strings. JavaScript converts the string `'3'` to a number and then subtracts 2.

    C. ` 3 + null`

    - output: `null` is treated as `0`, so adding 0 to 3 will result in `3`.

    D. ` '3' + null`

    - output: `'3null'`(string), Operands `'3'` is a string, `+` will concatenated with a string, `null` is coverted to the string, resulting the concatenation of the two strings.

    E. `true + 3`

    - output: `4`. since true maps to 1

    F. `false + null`

    - output: `0`. null treats as 0, false maps tp 0. so `0 + 0 = 0`

    G. `'3' + undefined`

    - output: `'3undefined'`. The `+` operator concatenation
      operator. If one of the operands `'3'` is a string, JavaScript will convert the other operand to a string as well and concatenate them.

    H. `'3' - undefined`

    - output:`NaN`. Since `undefined` is not a number, so trying to subtract it from anything results in NaN, which means "Not a Number".

- part2-question14

  - Comparison

    A. `'2' > 1`

    - output: `true`. When comparing values of different types, JavaScript converts the values to numbers. string `'2'` becomes a number 2

    B. `'2' < '12'`

    - output: `false`. When comparing strings, JavaScript performs a lexicographical comparison, character by character. Since `'2'` is lexicographically greater than `'12'`, so it output false.

    C. `2 == '2'`

    - output:`true`. When comparing values of different types, JavaScript converts the values to numbers. string '2' becomes a number 2.

    D. `2 === '2'`

    - output: `false`. `===` checks the equality without type conversion, number and string are different tpye.

    E. `true == 2`

    - output:`false`, `true` treats as `0` in number, 0 != 2

    F. `true === Boolean(2)`

    - output: `true`.Any non-zero number is true boolean type, and both side of `===` are true bool type.

- part2-question15

  - `==` is the equality operator and it performs type conversion if the two values are not of the same type. For example,`'01' == 1 ` will return ture, because `==` converts the values to numbers.
  - `===` is a strict equality operator, which checks the equality without type conversion.

- part2-question17

  It will return `[2, 4, 6]`. `modifyArray` function takes an array and a callback function as argument. It applies the callback function to each element of the array, and pushes the reslute to a new array, which then return.

  The `doSomething` function is defined to take a number and return that `number*2`

  Here is a quick walk through:

  1. `modifyArray` is invoked with the array [1, 2, 3] and doSomething as the callback.
  2. Inside modifyArray, a new empty array called `newArr` is created.
  3. In side the `for` loop, on the first iteration, i = 0,callback(array[i]) is `doSomething(array[0])` which returns 1\*2. The number `2` is then pushed to newArr. After the iteration, `newArr` now is `[2, 4, 6]`
  4. `modifyArray` returns this new array.

- part2-question19
  - output: `1 4 3 2`
