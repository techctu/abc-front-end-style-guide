##空白{#es5-space}
- 【**强制**】同一个项目内空白风格保持一致。

  ```javascript
  // bad
  function(){
      var name;
  }

  function() {
   var name;
  }

  // good
  function() {
    var name;
  }

  function() {
    var name;
  }
  ```
- 【**建议**】使用 2 个空格作为缩进。

  ```javascript
  // bad
  function () {
      var name;
  }

  // bad
  function () {
   var name;
  }

  // good
  function () {
    var name;
  }
  ```

- 【**建议**】在大括号前放一个空格。

  ```javascript
  // bad
  function test(){
    console.log('test');
  }

  // good
  function test() {
    console.log('test');
  }

  // bad
  dog.set('attr',{
    age: '1 year',
    breed: 'Bernese Mountain Dog'
  });

  // good
  dog.set('attr', {
    age: '1 year',
    breed: 'Bernese Mountain Dog'
  });
  ```

- 【**建议**】在控制语句（`if`、`while` 等）的小括号前放一个空格。在函数调用及声明中，不在函数的参数列表前加空格。

  ```javascript
  // bad
  if(isJedi) {
    fight ();
  }

  // good
  if (isJedi) {
    fight();
  }

  // bad
  function fight () {
    console.log ('Swooosh!');
  }

  // good
  function fight() {
    console.log('Swooosh!');
  }
  ```

- 【**建议**】使用空格把运算符隔开。

  ```javascript
  // bad
  var x=y+5;

  // good
  var x = y + 5;
  ```

- 【**建议**】在文件末尾插入一个空行。

  ```javascript
  // bad
  (function (global) {
    // ...stuff...
  })(this);
  ```

  ```javascript
  // bad
  (function (global) {
    // ...stuff...
  })(this);↵
  ↵
  ```

  ```javascript
  // good
  (function (global) {
    // ...stuff...
  })(this);↵
  ```

- 【**建议**】在使用长方法链时进行缩进。使用前面的点 `.` 强调这是方法调用而不是新语句。

  ```javascript
  // bad
  $('#items').find('.selected').highlight().end().find('.open').updateCount();

  // bad
  $('#items').
    find('.selected').
      highlight().
      end().
    find('.open').
      updateCount();

  // good
  $('#items')
    .find('.selected')
      .highlight()
      .end()
    .find('.open')
      .updateCount();

  // bad
  var leds = stage.selectAll('.led').data(data).enter().append('svg:svg').classed('led', true)
      .attr('width', (radius + margin) * 2).append('svg:g')
      .attr('transform', 'translate(' + (radius + margin) + ',' + (radius + margin) + ')')
      .call(tron.led);

  // good
  var leds = stage.selectAll('.led')
      .data(data)
    .enter().append('svg:svg')
      .classed('led', true)
      .attr('width', (radius + margin) * 2)
    .append('svg:g')
      .attr('transform', 'translate(' + (radius + margin) + ',' + (radius + margin) + ')')
      .call(tron.led);
  ```

- 【**建议**】在块末和新语句前插入空行。

  ```javascript
  // bad
  if (foo) {
    return bar;
  }
  return baz;

  // good
  if (foo) {
    return bar;
  }

  return baz;

  // bad
  var obj = {
    foo: function () {
    },
    bar: function () {
    }
  };
  return obj;

  // good
  var obj = {
    foo: function () {
    },

    bar: function () {
    }
  };

  return obj;
  ```