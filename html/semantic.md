## 语义化 {#html-semantic}

- 【**建议**】使用语义化的标签。没有 `CSS` 的 `HTML` 是一个语义系统，使用语义化有助于沟通和机器理解。如段落使用`p`，锚点使用`a`，按钮使用`button`。

  ```html
  <!-- Not recommended -->
  <div onclick="">点击按钮</div>
  <div onclick="goToRecommendations();">All recommendations</div>

  <!-- Recommended -->
  <button onclick="">点击按钮</button>
  <a href="recommendations/">All recommendations</a>

  <!-- Recommended -->
  <h1>一级标题</h1>
  <h2>二级标题</h2>
  <p>一段文字</p>
  <ul>
        <li>列表</li>
        <li>无序</li>
  </ul>
  <ol>
        <li>有序</li>
        <li>列表</li>
  </ol>
  <blockquote>一大段引用</blockquote>
  <cite>一般引用</cite>
  <b>为样式加粗</b>
  <strong>为强调内容加粗</strong>
  <i>为样式倾斜</i>
  <em>为强调内容倾斜</em>
  <div>code:代码标识 abbr:缩写</div>
  ```
