#### 返回恰当的状态码


每个响应返回适当的HTTP状态代码。成功响应应根据本指南进行编码：

* `200`: 请求成功执行`GET`，`POST`，`DELETE`或`PATCH`调用同步完成，或同步更新的“PUT”调用现有资源
* `201`: 请求成功进行同步的“POST”或“PUT”调用创建了一个新资源。提供“Location”也是最佳做法标题指向新创建的资源。这特别有用在`POST`上下文中，因为新资源的URL将不同于原始要求
* `202`: 请求接受“POST”，“PUT”，“DELETE”或“PATCH”调用，这些调用将异步处理
* `206`: `GET`请求成功, 但只是部分响应
  参见: see [above on ranges](../foundations/divide-large-responses-across-requests-with-ranges.md)

注意使用身份验证和授权错误代码

* `401 Unauthorized`: 请求失败因为用户未通过身份验证
* `403 Forbidden`: 请求失败因为用户无权限访问特定资源

但出现错误时，返回合适的状态码以及提示信息：

* `422 Unprocessable Entity`: 您的请求以被理解，但包含无效参数
* `429 Too Many Requests`: 您已受到速率限制，请稍后访问
* `500 Internal Server Error`: 服务器出错，检查状态站点和/或报告问题

相关文章 [HTTP response code spec](https://tools.ietf.org/html/rfc7231#section-6)
用户出错或服务器出错的状态码处理
