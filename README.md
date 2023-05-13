## 介绍

配置了原生+tailwindcss的最简单的启动模板。

启动项目：

pnpm i

pnpm watch



## 该项目的创建过程
依赖清单：

1. pnpm
2. lite-server
3. npm-run-all
4. tailwindcss



创建过程：

1. 安装pnpm、lite-server
`npm i pnpm lite-server -g`
2. 创建项目
`pnpm init`
`pnpm i tailwindcss npm-run-all -D`
`npx tailwindcss init`
3. 配置文件

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['*.html'],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

4. 配置脚本

```
    "watch:tw": "npx tailwindcss -o tailwind.css --watch",
    "watch:html": "npx lite-server",
    "watch": "run-p watch:tw watch:html"
```

5. 编写html

```
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="stylesheet" href="tailwind.css">
</head>

<body>
</body>
</html>
```

