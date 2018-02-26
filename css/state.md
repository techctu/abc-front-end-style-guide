## 声明{#css-state}
- 【**建议**】使用语义化、通用的命名方式，组件样式突出组件状态，页面样式突出页面业务状态。

  ```css
  /* Not recommended: 无意义 */
  #yee-1901 {}

  /* Not recommended: 展示状态非业务状态 */
  .button-green {}
  .clear {}

  /* Recommended: 业务状态-特定 */
  #gallery {}
  #login {}
  .video {}

  /* Recommended: 业务状态-通用 */
  .aux {}
  .alt {}
  ```
  
- 【**强制**】使用小写字母。

  ```css
  /* Not recommended */
  .Red {}
  
  /* Recommended */
  .red {}
  ```

- 【**强制**】使用连字符 `-` 作为 ID、Class 名称界定符，不要驼峰命名法和下划线。

  ```css
  /* Not recommended */
  .buziError {}
  .Buzi_Error {}
  
  /* Recommended */
  .buzi-error {}
  ```

- 【**建议**】出于性能考量，不要使用元素选择器叠加 Class、ID 使用。

  ```css
  /* Not recommended */
  ul#example {}
  div.error {}
  
  /* Recommended */
  #example {}
  .error {}
  ```
    
- 【**建议**】适当使用简写。

    ```css
    /* Not recommended */
    #navigation {}
    .atr {}
    
    /* Recommended */
    #nav {}
    .author {}
    ```

- 【**强制**】选择器分组时，保持独立的选择器占用一行。
- 【**强制**】声明块的左括号 `{` 前添加一个空格。
- 【**强制**】声明块的右括号 `}` 应单独成行。
- 【**强制**】声明语句中的 `:` 后应添加一个空格。
- 【**强制**】声明语句应以分号 `;` 结尾。
- 【**强制**】一般以逗号分隔的属性值，每个逗号后应添加一个空格。
- 【**强制**】`rgb()、rgba()、hsl()、hsla() 或 rect()` 括号内的值，逗号分隔，但逗号后不添加一个空格。
- 【**强制**】对于属性值或颜色参数，省略小于 1 的小数前面的 0 （例如，`.5` 代替 `0.5`；`-.5px` 代替 `-0.5px`）。
- 【**强制**】十六进制值应该全部小写和尽量简写，例如，`#fff` 代替 `#ffffff`。
- 【**强制**】避免为 0 值指定单位，例如，用 `margin: 0;` 代替 `margin: 0px;`。
- 【**强制**】行尾和换行避免多余的空格。

  ```css
    /* Not recommended  */
  .selector, .selector-secondary, .selector[type=text] {
    padding:15px;
    margin:0px 0px 15px;
    background-color:rgba(0, 0, 0, 0.5);
    box-shadow:0px 1px 2px #CCC,inset 0 1px 0 #FFFFFF
  }

  /* Recommended */
  .selector,
  .selector-secondary,
  .selector[type="text"] {
    padding: 15px;
    margin-bottom: 15px;
    background-color: rgba(0,0,0,.5);
    box-shadow: 0 1px 2px #ccc, inset 0 1px 0 #fff;
  }
  ```
- 【**建议**】当出现多个嵌套的时候容易失去控制，应保持不超过一个嵌套。
- 【**建议**】避免使用标签选择器。
- 【**建议**】尽量使用其他的方式而不是 hack。如果要使用 hack，一定要注释清晰。