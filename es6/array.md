## 数组{#es6-array}
- 【**建议**】使用字面值创建数组。

  ```javascript
  // bad
  const items = new Array();

  // good
  const items = [];
  ```

- 【**建议**】向数组添加元素时使用 Arrary#push 替代直接赋值。

  ```javascript
  const someStack = [];

  // bad
  someStack[someStack.length] = 'abracadabra';

  // good
  someStack.push('abracadabra');
  ```

- 【**建议**】使用拓展运算符 `...` 复制数组。

  ```javascript
  // bad
  const len = items.length;
  const itemsCopy = [];
  let i;

  for (i = 0; i < len; i++) {
    itemsCopy[i] = items[i];
  }

  // good
  const itemsCopy = [...items];
  ```
