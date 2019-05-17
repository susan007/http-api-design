#### 为方便起见，支持非id解除引用


在某些情况下，最终用户提供ID来识别资源可能不方便。例如，用户可能会想到Heroku应用程序名称的条款，但该应用程序可能由UUID标识。在这些情况下，您可能希望同时接受id或名称，例如：

```bash
$ curl https://service.com/apps/{app_id_or_name}
$ curl https://service.com/apps/97addcf0-c182
$ curl https://service.com/apps/www-prod
```

不要只接受名称以排除ID。
