##运算符{#es5-operator}
- 【**建议**】优先使用 `===` 和 `!==` 而不是 `==` 和 `!=`.

- 【**建议**】使用快捷方式。
  > 条件表达式例如 `if` 语句通过抽象方法 `ToBoolean` 强制计算它们的表达式并且总是遵守下面的规则：
  > + **对象** 被计算为 **true**
  > + **Undefined** 被计算为 **false**
  > + **Null** 被计算为 **false**
  > + **布尔值** 被计算为 **布尔的值**
  > + **数字** 如果是 **+0、-0 或 NaN** 被计算为 **false**，否则为 **true**
  > + **字符串** 如果是空字符串 `''` 被计算为 **false**，否则为 **true**

  ```javascript
  // bad
  if (name !== '') {
    // ...stuff...
  }

  // good
  if (name) {
    // ...stuff...
  }

  // bad
  if (collection.length > 0) {
    // ...stuff...
  }

  // good
  if (collection.length) {
    // ...stuff...
  }
  ```