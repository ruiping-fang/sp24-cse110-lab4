- part1-question1
  - line 9 will print:
  ```javascript
      values added: 20
  ```
- part1-question2

  - line 13 will print

  ```javascript
      final results: 20
  ```

- part1-question3

  - line 9 will print:

  ```javascript
      values added: 20
  ```

- part1-question4

  - The code returns an error because the `result` in line 13 is not defined. The variable `result` is declared with `let` inside the `if` block, which means its scope is limited to that block. Because of this, when the `console.log('final resulte:', result);` line try to access `resulte` outside of the block where it was defined, it throws an error.

- part1-question5

  - `const` must be initialized at the time of declaration and cannot be reassigned. There's an attempt to reassign `result` after it has been declared with `const`, which will cause an error. Therefore, line 9 won't be reached, and nothing will be printed because an error will occur at line 6 when trying to reassign result

- part1-question6

  - Line 13 will not print anything and will cause an error. The variable `result` is declared with `const` within the `if` block, which limits its scope to that block. Therefore, result is not accessible outside of the `if` block, where line 13 is trying to reference it.
