## 引用{#es6-ref}

- 【**强制**】对常量引用使用 `const` ；不要使用 `var`。

  ```javascript
  // bad
  var a = 1;
  var b = 2;

  // good
  const a = 1;
  const b = 2;
  ```

- 【**强制**】对变量引用，使用 `let`； 不要使用 `var`。

  > 为什么？因为  `let` 和 `const` 是块级作用域，而 `var` 是函数作用域。

  ```javascript
  // bad
  var count = 1;
  if (true) {
    count += 1;
  }

  // good, use the let.
  let count = 1;
  if (true) {
    count += 1;
  }
  ```
