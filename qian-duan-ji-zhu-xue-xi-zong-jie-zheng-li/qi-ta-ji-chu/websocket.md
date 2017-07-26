#WebSocket

##什么是WebSocket？
WebSocket 是一种**网络通信协议**。

**HTTP 协议有一个缺陷：通信只能由客户端发起。做不到服务器主动向客户端推送信息**。

如果**服务器有连续的状态变化，客户端要获知就很麻烦**。**只能使用"轮询"**：每隔一段时候，就发出一个询问，了解服务器有没有新的信息。最典型的场景就是聊天室。

**轮询的效率低，非常浪费资源（因为必须不停连接**，或者 HTTP 连接始终打开）。

WebSocket 协议2011年成为国际标准。所有浏览器都已经支持了。

它的**最大特点是，服务器可以主动向客户端推送信息，客户端也可以主动向服务器发送信息**，是真正的双向平等对话，属于[服务器推送技术](https://en.wikipedia.org/wiki/Push_technology)的一种。

##webSocket的特点

特点包括：
（1）服务器可以主动向客户端推送信息，客户端也可以主动向服务器发送信息。
（2）**建立在 TCP 协议上**，服务器端的实现比较容易。
（3）**与 HTTP 协议有良好的兼容性。默认端口也是80和443，并且握手阶段采用 HTTP 协议**，因此握手时不容易屏蔽，能通过各种 HTTP 代理服务器。
（4）数据格式较轻量，性能开销小，通信高效。
（5）可以发送文本，也可以发送二进制数据。
（6）**没有同源限制，客户端可以与任意服务器通信**。
（7）**协议标识符是ws（如果加密，则为wss）**，服务器网址就是 URL（如：ws://example.com:80/some/path）。

参考资源：
[WebSocket 教程（阮一峰）](http://www.ruanyifeng.com/blog/2017/05/websocket.html)

http://websocket.org/
