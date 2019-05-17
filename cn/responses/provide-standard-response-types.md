#### 提供标准响应体类型


本文档描述了每种JSON基本数据类型的可接受值。

### 字符串

* 可接受的值：
  * string
  * `null`

例如：

```javascript
[
  {
    "description": "very descriptive description."
  },
  {
    "description": null
  },
]
```

### 布尔类型

* 可接受的值：
  * true
  * false

例如：

```javascript
[
  {
    "provisioned_licensese": true
  },
  {
    "provisioned_licenses": false
  },
]
```

### 数字类型

* 可接受值：
  * number
  * `null`

注意：某些JSON解析器将返回精度超过15的数字小数位作为字符串。如果您需要大于15位小数的精度，始终返回该值的字符串。如果没有，请将这些字符串转换为数字，
以便API的消费者始终知道期望的值类型。

例如：

```javascript
[
  {
    "average": 27.123
  },
  {
    "average": 12.123456789012
  },
]
```

### 数组

* 可接受值：
  * array

注意：当数组中没有值时，返回一个空数组而不是“NULL”。

例如：

```javascript
[
  {
    "child_ids": [1, 2, 3, 4],
  },
  {
    "child_ids": [],
  }
]
```

### 对象

* 可接受值：
  * object
  * null

例如：

```javascript
[
  {
    "name": "service-production",
    "owner": {
      "id": "5d8201b0..."
     }
  },
  {
    "name": "service-staging",
    "owner": null
  }
]
```
