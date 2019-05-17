#### 在所有响应中削减JSON

额外的空白会为请求添加不必要的响应大小，以及许多人类消费的客户将自动“美化”JSON输出。
最好将JSON响应缩小，例如：

```json
{"beta":false,"email":"alice@heroku.com","id":"01234567-89ab-cdef-0123-456789abcdef","last_login":"2012-01-01T12:00:00Z","created_at":"2012-01-01T12:00:00Z","updated_at":"2012-01-01T12:00:00Z"}
```

而非如下：

```json
{
  "beta": false,
  "email": "alice@heroku.com",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "last_login": "2012-01-01T12:00:00Z",
  "created_at": "2012-01-01T12:00:00Z",
  "updated_at": "2012-01-01T12:00:00Z"
}
```


您可以考虑为客户端提供一种检索方式，更详细的响应，通过查询参数（例如`？pretty = true`）
或通过`Accept`标题参数（例如`Accept: application/vnd.heroku+json; version=3; indent=4;`).
