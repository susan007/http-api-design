#### 分离关注


通过分离问题之间的关注，在设计时保持简单请求和响应周期的不同部分。
在这里保持简单的规则允许更多地关注更大和更难的问题。


将提出请求体和响应体以解决特定资源或采集。
使用路径表示身份，身体转移用于传达元数据的内容和标题。
查询参数可以用作a表示在边缘情况下也传递标题信息，但首选标题因为它们更灵活，可以传达更多样化的信息。