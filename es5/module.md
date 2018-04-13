##模块{#es5-module}
- 【**强制**】模块应该以 `!` 开始。这样确保了当一个不好的模块忘记包含最后的分号时，在合并代码到生产环境后不会产生错误。
- 【**强制**】文件应该以驼峰式命名，并放在同名的文件夹里，且与导出的名字一致。
- 【**强制**】增加一个名为 `noConflict()` 的方法来设置导出的模块为前一个版本并返回它。
- 【**强制**】永远在模块顶部声明 `'use strict';`。

  ```javascript
  // fancyInput/fancyInput.js

  !function (global) {
    'use strict';

    var previousFancyInput = global.FancyInput;

    function FancyInput(options) {
      this.options = options || {};
    }

    FancyInput.noConflict = function noConflict() {
      global.FancyInput = previousFancyInput;
      return FancyInput;
    };

    global.FancyInput = FancyInput;
  }(this);
  ```