##命名{#es5-naming}
- 【**强制**】避免单字母命名。命名应具备描述性。

  ```javascript
  // bad
  function q() {
    // ...stuff...
  }

  // good
  function query() {
    // ..stuff..
  }
  ```

- 【**强制**】使用驼峰式命名对象、函数和实例。

  ```javascript
  // bad
  var OBJEcttsssss = {};
  var this_is_my_object = {};
  var o = {};
  function c() {}

  // good
  var thisIsMyObject = {};
  function thisIsMyFunction() {}
  ```

- 【**强制**】使用帕斯卡式命名构造函数或类。

  ```javascript
  // bad
  function user(options) {
    this.name = options.name;
  }

  var bad = new user({
    name: 'nope'
  });

  // good
  function User(options) {
    this.name = options.name;
  }

  var good = new User({
    name: 'yup'
  });
  ```

- 【**强制**】不要使用下划线前/后缀。

  > 为什么？JavaScript 并没有私有属性或私有方法的概念。虽然使用下划线是表示「私有」的一种共识，但实际上这些属性是完全公开的，它本身就是你公共接口的一部分。这种习惯或许会导致开发者错误的认为改动它不会造成破坏或者不需要去测试。长话短说：如果你想要某处为「私有」，它必须不能是显式提出的。

  ```javascript
  // bad
  this.__firstName__ = 'Panda';
  this.firstName_ = 'Panda';
  this._firstName = 'Panda';

  // good
  this.firstName = 'Panda';
  ```

- 【**强制**】不要保存 `this` 的引用。使用 Function#bind。

  ```javascript
  // bad
  function () {
    var self = this;
    return function () {
      console.log(self);
    };
  }

  // bad
  function () {
    var that = this;
    return function () {
      console.log(that);
    };
  }

  // bad
  function () {
    var _this = this;
    return function () {
      console.log(_this);
    };
  }

  // good
  function () {
    return function () {
      console.log(this);
    }.bind(this);
  }
  ```

- 【**强制**】给函数命名。这在做堆栈轨迹时很有帮助。

  ```javascript
  // bad
  var log = function (msg) {
    console.log(msg);
  };

  // good
  var log = function log(msg) {
    console.log(msg);
  };
  ```

  > **注：** IE8 及以下版本对命名函数表达式的处理有些怪异。了解更多信息到 [http://kangax.github.io/nfe/](http://kangax.github.io/nfe/)。

- 【**强制**】如果你的文件导出一个类，你的文件名应该与类名完全相同。
  ```javascript
  // file contents
  class CheckBox {
    // ...
  }
  module.exports = CheckBox;

  // in some other file
  // bad
  var CheckBox = require('./checkBox');

  // bad
  var CheckBox = require('./check_box');

  // good
  var CheckBox = require('./CheckBox');
  ```