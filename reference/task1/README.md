# Task 1 指导（24 分）：Express Hello World

## 目标
建 `~/task1` 文件夹，写 `server.js` 和 `package.json`，`npm start` 后浏览器访问 `localhost:8099` 看到 Hello World!。

## 步骤

```bash
cd ~
mkdir task1
cd task1
nano server.js
nano package.json
npm install
npm start
```

浏览器（Ubuntu 内的 Firefox）打开 http://localhost:8099，看到 Hello World!。

## 文件内容

`server.js`：

```javascript
const express = require('express')
const app = express()
const port = process.env.PORT || 8099

app.get('/', (req, res) => {
  res.send('Hello World!')
})

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
})
```

`package.json`（把 author 改成你的全名）：

```json
{
  "name": "A Node.js App",
  "description": "LabExercise 1-Task1",
  "author": "你的全名",
  "version": "0.0.1",
  "dependencies": { "express": "*" },
  "engine": "*",
  "scripts": { "start": "node server.js" }
}
```

## CHECK points（考官看的）

- 工作路径/文件夹 `~/task1` 正确 —— 2 分
- 文件已创建（server.js、package.json）—— 2 分
- 运行命令及结果（npm install / npm start）—— 4 分
- 浏览器测试结果（Hello World!）—— 2 分
- 文件内容（两份文件里的代码）—— 14 分
