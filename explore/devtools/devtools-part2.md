1. What was the bug?

   The values retrieved from the input fields
   `getElementById("num1").value `and `getElementById("num2").value)` are strings, not numbers. so `num1` and `num2` will be strings.

2. How would you fix it?

   To fix the bug, I convert the input values to numbers before adding them, where I use `parseFloat`

   ```javascript
   let num1 = parseFloat(document.getElementById("num1").value);
   let num2 = parseFloat(document.getElementById("num2").value);
   ```
