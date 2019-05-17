#### 需要安全连接


需要与TLS的安全连接才能访问API，无一例外。
不值得尝试弄清楚或解释什么时候可以使用TLS，什么时候不行。
只需要TLS就可以了。


理想情况下，通过不响应对http或端口80的请求来简单地拒绝任何非TLS请求，以避免任何不安全的数据交换。
在无法做到这一点的环境中，请回复“403 Forbidden”。


不鼓励重定向，因为它们允许草率/糟糕的客户行为而不提供任何明显的收益。
依赖重定向的客户端会增加服务器流量并使TLS无效，因为在第一次调用期间已经暴露了敏感数据。