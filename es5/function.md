##函数{#es5-function}

- 【**强制**】永远不要在一个非函数代码块（if、while 等）中声明一个函数，浏览器允许你这么做，但它们的解析表现不一致，正确的做法是：在块外定义一个变量，然后将函数赋值给它。
  > **注：** ECMA-262 把 `块` 定义为一组语句。函数声明不是语句。

  ```javascript
  // bad
  if (currentUser) {
    function test() {
      console.log('Nope.');
    }
  }

  // good
  var test;
  if (currentUser) {
    test = function test() {
      console.log('Yup.');
    };
  }
  ```

- 【**强制**】永远不要把参数命名为 `arguments`。这将取代函数作用域内的 `arguments` 对象。

  ```javascript
  // bad
  function nope(name, options, arguments) {
    // ...stuff...
  }

  // good
  function yup(name, options, args) {
    // ...stuff...
  }
  ```