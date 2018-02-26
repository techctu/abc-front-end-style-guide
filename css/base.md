## 通常
- 【**建议**】以组件为单位组织代码段。
- 【**建议**】如果使用了多个 CSS 文件，将其按照组件而非页面的形式分拆，因为页面会被重组，而组件只会被移动。
- 【**强制**】文件使用 `utf-8` 编码，**不要使用 utf-8 with BOM**。
- 【**建议**】尽可能使用 HTTPS 协议，除非依赖的资源无法通过 HTTPS 获取。
  
  ```css
  /* Not recommended: omits the protocol */
  @import '//fonts.googleapis.com/css?family=Open+Sans';

  /* Not recommended: uses the HTTP protocol */
  @import "http://fonts.googleapis.com/css?family=Open+Sans";

  /* Recommended */
  @import "https://fonts.googleapis.com/css?family=Open+Sans";
  ```