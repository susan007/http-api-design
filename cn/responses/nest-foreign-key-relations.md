#### 嵌套外键关系

使用嵌套对象序列化外键引用，例如：

```javascript
{
  "name": "service-production",
  "owner": {
    "id": "5d8201b0..."
  },
  // ...
}
```

而非如下：

```javascript
{
  "name": "service-production",
  "owner_id": "5d8201b0...",
  // ...
}
```

这种方法可以内联有关的更多信息相关资源，而无需更改响应的结构或引入更多顶级响应字段，例如：

```javascript
{
  "name": "service-production",
  "owner": {
    "id": "5d8201b0...",
    "email": "alice@heroku.com"
  },
  // ...
}
```

嵌套外键关系时，请使用完整记录或仅使用外键。提供字段子集可能会导致意外和混淆，使得不同操作和端点之间的不一致更有可能。

为避免不一致和混淆，请序列化：
- **仅限外键**  - 可以查看完整记录的值，例如`id`，`slug`，`email`
- **完整记录**，所有字段（这将是“嵌入式记录”）
