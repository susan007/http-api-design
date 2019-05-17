#### 尽可能提供全部资源

提供完整的资源表示（即包含所有对象的对象）属性）尽可能在响应中。
始终提供完整200和201响应的资源，包括`PUT` /`PATCH`和`DELETE`请求，例如：

```bash
$ curl -X DELETE \
  https://service.com/apps/1f9b/domains/0fd4

HTTP/1.1 200 OK
Content-Type: application/json;charset=utf-8
...
{
  "created_at": "2012-01-01T12:00:00Z",
  "hostname": "subdomain.example.com",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

202回复将不包括完整的资源代表，
例如。：

```bash
$ curl -X DELETE \
  https://service.com/apps/1f9b/dynos/05bd

HTTP/1.1 202 Accepted
Content-Type: application/json;charset=utf-8
...
{}
```
