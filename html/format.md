## 代码格式{#html-format}
- 【**建议**】为代码添加注释，指明目的、范围、原因。
  ```html
  <!-- Not recommended: 大段代码无注释 -->
  <ul>
    <li>Apples</li>
    <li>Oranges</li>
  </ul>

  <!-- Recommended -->
  <!-- 显示商品列表 -->
  <ul>
    <li>Apples</li>
    <li>Oranges</li>
  </ul>
  ```

- 【**建议**】使用`TODO`来标明待完成项。

  ```html
  <!-- Recommended -->
  <!-- TODO: remove optional tags -->
  <ul>
    <li>Apples</li>
    <li>Oranges</li>
  </ul>
  ```

- 【**强制**】同一个项目内缩进需要保持一致。

  ```html
  <!-- Not recommended -->
  <!-- File a -->
  <ul>
    <li>Apples</li>
    <li>Oranges</li>
  </ul>
  <!-- File b -->
  <ul>
      <li>Apples</li>
      <li>Oranges</li>
  </ul>

  <!-- Recommended -->
  <!-- File a -->
  <ul>
    <li>Apples</li>
    <li>Oranges</li>
  </ul>
  <!-- File b -->
  <ul>
    <li>Apples</li>
    <li>Oranges</li>
  </ul>
  ```

- 【**建议**】使用2个空格缩进。

  ```html
  <!-- Recommended -->
  <ul>
    <li>Fantastic
    <li>Great
  </ul>
  ```
  
- 【**强制**】使用小写字母。

  ```html
  <!-- Not recommended -->
  <A HREF="/">Home</A>
  
  <!-- Recommended -->
  <img src="google.png" alt="Google" />
  ```

- 【**强制**】ID 使用小写字母和连字符`-`构成，不要使用下划线`_`。

- 【**强制**】移除末尾空格。此处用下划线`_`表示末尾空格。

  ```html
  <!-- Not recommended -->
  <p>What?_
  
  <!-- Recommended -->
  <p>Yes please.
  ```

- 【**建议**】为多媒体资源提供`alt`。

  ```html
  <!-- Not recommended -->
  <img src="spreadsheet.png" >
  
  <!-- Recommended -->
  <img src="spreadsheet.png" alt="Spreadsheet screenshot.">
  ```
  
- 【**建议**】不闭合空标签。早期出于对严格符合 XML 的执着要求闭合标签，现在最新官方标准明确表示 `/` 对空标签无效。添加 `/` 不会导致解析出错。

  ```html
  <!-- Not recommended -->
  <img src="spreadsheet.png" alt="Spreadsheet screenshot."/>
  
  <!-- Recommended -->
  <img src="spreadsheet.png" alt="Spreadsheet screenshot.">
  ```

- 【**建议**】尽可能减少标签数量。

  ```html
  <!-- Not recommended -->
  <span class="avatar">
    <img src="assets/img/img.png" alt="Jane Doe">
  </span>
  
  <!-- Recommended -->
  <img class="avatar" src="assets/img/img.png" alt="Jane Doe">
  ```

- 【**建议**】不要使用符号实体，除非要用到 `<` 等。

  ```html
  <!-- Not recommended -->
  <p>
    The currency symbol for the Euro is &ldquo;&eur;&rdquo;.
  </p>

  <!-- Recommended -->
  <p>
    The currency symbol for the Euro is “€”.
  </p>
  ```

  ```html
  <!-- Not recommended: 使用了 < 导致解析和代码高亮出现异常 -->
  <p>
    1 < 2
  </p>
  
  <!-- Recommended -->
  <p>
    1 &lsaquo; 2
  </p>
  ```

- 【**建议**】标签属性顺序如下排列。
  + id
  + class
  + name
  + data-xxx
  + src, for, type, href
  + title, alt
  + aria-xxx, role

  ```html
  <!-- Recommended -->
  <a id="..." class="..." data-modal="..." href="..."></a>
  <input class="..." type="text">
  <img src="..." alt="...">
  ```

- 【**强制**】属性使用双引号。

  ```html
  <!-- Not recommended -->
  <img src='spreadsheet.png' alt='Spreadsheet screenshot.'/>
  
  <!-- Recommended -->
  <img src="spreadsheet.png" alt="Spreadsheet screenshot.">
  ```

- 【**强制**】HTML5 规范中的 `disabled checked selected` 等布尔值属性无需赋值。

  ```html
  <!-- Not recommended -->
  <img src="spreadsheet.png" disabled="true">
  <img src="spreadsheet.png" disabled="false">

  <!-- Recommended -->
  <input type="text" disabled>
  <input type="text">
  ```