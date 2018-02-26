# 前端代码风格指南

中国农业银行总行软件开发中心代码风格指南。

## 内容说明
- HTML 代码风格指南：包含HTML相关的风格指南，请注意与各类模板语法标签的区分，如 velocity、JSX 等。
- CSS 代码风格指南：包含CSS相关的风格指南，请注意与 LESS、SASS、SCSS 等的区分。
- ECMAScript 5 代码风格指南：目前[浏览器支持](https://caniuse.com/#search=ECMAScript%205)最广泛的 JavaScript 代码风格指南，IE8及以下请使用针对性的 [polyfill](GLOSSARY.md#polyfill)。
- ECMAScript 2015 代码风格指南：泛指 ES 已经到来的下一代 JavaScript 代码风格指南，

## 格式说明

* **强调**：**这样的文字内容表示强调。**
* `强调-代码`：`这样的内容表示引用，一般用于强调风格指南相关的语言关键词、属性等，如 class、const`。
* 指南规则分为**强制**和**建议**。
* 指南示例代码分为**差**，**好**两种。在代码注释中进行说明。不是所有的指南都有代码示例。
  ```js
  // 差（bad/not recommended）
  var item = new Object();
  // 好（good/recommended）
  var item = {};
  ```
