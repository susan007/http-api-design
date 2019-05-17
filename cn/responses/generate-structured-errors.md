#### 生成结构化错误

在错误上生成一致的，结构化的响应主体。包括一个机器可读的错误`id`，一个人类可读的错误`message`，和可选地，“url”指向客户端以获得有关的更多信息错误以及如何解决它，例如：

```
HTTP/1.1 429 Too Many Requests
```

```json
{
  "id":      "rate_limit",
  "message": "Account reached its API rate limit.",
  "url":     "https://docs.service.com/rate-limits"
}
```

记录您的错误格式以及客户可能遇到的错误`id`s。
