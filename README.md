# 聊天吧
通过socket.io实现即时通讯功能的小练习。

#### 聊天吧介绍
- 服务端（server） server.js
- 客户端（client） chat.js
- 用到所需依赖
  - koa
  - koa-static
  - socket.io
  - moment
#### 需求列表：
- 当前用户和其他用户都可以看到发送的消息
  - 搭建 websocket 服务器
  - client 连接到 server 端
  - 可以访问 /chat.html
  - 点击发送按钮 server 端可以收到消息
  - 发送完输入框要清空
  - 基于后端发过来的消息进行前端渲染 - 生成一个 div
  - 让其他用户也能收到消息
- 消息显示用户名和发送的时间
  - 解析 querystring
  - 需要把 username 给到 server 端
  - server 端需要把数据给到 client 端（包括所有的用户）
- 用户进入聊天室的时候
  - 当前用户提示 - 欢迎来到聊天室
  - 其他用户提示 - xxx 加入了聊天室
- 房间
  - 只有在同一房间内的用户才可以收到消息
  - 不同房间的用户不可以收到消息
- 显示房间名
- 显示用户列表
  - 有用户加入的时候，用户列表要实时刷新
  - 有用户离开的时候，用户列表要实时刷新
- 用户离开聊天室的时候
  - 其他用户提示 - xxx 离开了聊天室
