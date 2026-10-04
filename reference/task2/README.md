# Task 2 指导（16 分）：OpenWeather 天气 API

## 目标
建 `~/task2` 文件夹，下载样例 `server.js`，填入你的 OpenWeather API key，运行后打印东京天气 JSON。

## 前提
提前准备有效的 OpenWeather API key（考官不帮忙）。注册：https://home.openweathermap.org/users/sign_up

## 步骤

```bash
cd ~
mkdir task2
cd task2
```

下载样例 server.js（用 raw 链接）：

```bash
curl -L -o server.js https://raw.githubusercontent.com/yalin-liu/cloudserver-2026/main/exe01/server.js
```

验证：

```bash
ls
cat server.js
```

填入 API key：

```bash
nano server.js
```

把这一行改成你的 key：

```javascript
const APIKEY='77b62358916e3fabc27c3d884560f2d7';//**your API key***
```

保存（Ctrl+O → 回车 → Ctrl+X），运行：

```bash
node server.js
```

看到终端打印东京天气 JSON（含 `"name":"Tokyo"`、`"cod":200`）即成功。

## CHECK points（考官看的）

- 工作路径/文件夹 `~/task2` 正确 —— 4 分
- `~/task2/server.js` 存在 —— 4 分
- 终端运行结果（天气 JSON）—— 4 分
- 文件内容（含 API key 的 server.js）—— 4 分
