#### 在请求正文中接受序列化的JSON

接受`PUT` /`PATCH` /`POST`请求​​体上的序列化JSON代替形式编码数据或者除了形式编码数据之外。这创造了对称性与JSON序列化的响应主体，例如：

```bash
$ curl -X POST https://service.com/apps \
    -H "Content-Type: application/json" \
    -d '{"name": "demoapp"}'

{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "name": "demoapp",
  "owner": {
    "email": "username@example.com",
    "id": "01234567-89ab-cdef-0123-456789abcdef"
  },
  ...
}
```
