## HEAD {#html-head}

- 【**强制**】使用 `<!DOCTYPE html>`。

- 【**强制**】使用 `lang="zh-cmn"`。

- 【**强制**】使用 `utf-8` 编码并作为 `head` 的第一个子元素。
  ```html
  <!-- Recommended -->
  <html>
    <head>
      <meta charset="utf-8">
    </head>
  </html>
  ```

- 【**强制**】优先使用最新版本 IE 和 Chrome 内核。
  ```html
  <!-- Recommended -->
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
  ```

- 【**建议**】SEO 优化。
  ```html
  <!-- Recommended -->
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <!-- SEO -->
    <title>标题</title>
    <meta name="keywords" content="关键词">
    <meta name="description" content="简介">
    <meta name="author" content="author,email address">
  </head>
  ```

- 【**建议**】为移动端设备优化，设置可见区域的宽度和初始缩放比例。

  ```html
  <!-- Recommended -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```

- 【**建议**】设置 iOS 图标。

  ```html
  <!-- Recommended -->
  <!-- iPhone 和 iTouch，默认 57x57 像素，必须有 -->
  <link rel="apple-touch-icon-precomposed" href="/apple-touch-icon-57x57-precomposed.png">

  <!-- iPad，72x72 像素，可以没有，但推荐有 -->
  <link rel="apple-touch-icon-precomposed" href="/apple-touch-icon-72x72-precomposed.png" sizes="72x72">

  <!-- Retina iPhone 和 Retina iTouch，114x114 像素，可以没有，但推荐有 -->
  <link rel="apple-touch-icon-precomposed" href="/apple-touch-icon-114x114-precomposed.png" sizes="114x114">

  <!-- Retina iPad，144x144 像素，可以没有，但推荐有 -->
  <link rel="apple-touch-icon-precomposed" href="/apple-touch-icon-144x144-precomposed.png" sizes="144x144">
  ```

- 【**建议**】指定 favicon 。

  ```html
  <!-- Recommended -->
  <link rel="shortcut icon" href="path/to/favicon.ico">
  ```

- 【**建议**】使用 HEAD 模板。

  ```html
  <!-- Recommended -->
  <!DOCTYPE html>
  <html lang="zh-CN">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <title>Style Guide</title>
    <meta name="description" content="不超过150个字符">
    <meta name="keywords" content="">
    <meta name="author" content="name, email@gmail.com">

    <!-- 为移动设备添加 viewport -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!-- iOS 图标 -->
    <link rel="apple-touch-icon-precomposed" href="/apple-touch-icon-57x57-precomposed.png">

    <link rel="alternate" type="application/rss+xml" title="RSS" href="/rss.xml" />
    <link rel="shortcut icon" href="path/to/favicon.ico">
  </head>
  ```
  
- 【**强制**】如果引入的是 `.css` 文件或者 `.js` 文件，无需指定 `type` 。