##对象{#es5-object}

- 【**强制**】不要使用保留字作为键名，它们在 IE8 下不工作。

  ```javascript
  // bad
  var superman = {
    default: { clark: 'kent' },
    private: true
  };

  // good
  var superman = {
    defaults: { clark: 'kent' },
    hidden: true
  };
  ```

  ```
  // 保留字
  break do instanceof typeof case else new var catch finally return void continue for switch while debugger function this with default if throw delete in try class enum extends super const export import implements let private public yield interface package protected static
  ```

- 【**建议**】使用字面量创建对象。

  ```javascript
  // bad
  var item = new Object();

  // good
  var item = {};
  ```
