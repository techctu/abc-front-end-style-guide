## 文档与协议 {#html-standard}

* 【**强制**】使用 UTF-8 编码，**不要使用 UTF8 with BOM**。
* 【**建议**】尽可能使用 HTTPS 协议，除非依赖的资源无法通过 HTTPS 获取。 
  ```html
  <!-- Not recommended: 忽略了协议 -->
  <script src="//ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js"></script>

  <!-- Not recommended: HTTP -->
  <script src="http://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js"></script>
  
  <!-- Recommended -->
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js"></script>
  ```



