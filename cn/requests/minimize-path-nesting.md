#### 最小路径嵌套

在具有嵌套父/子资源关系的数据模型中，路径可能会变得深层嵌套，例如：

```
/orgs/{org_id}/apps/{app_id}/dynos/{dyno_id}
```


通过优先在根位置定位资源来限制嵌套深度路径。使用嵌套来指示范围集合。例如，对于dyno属于app的上述情况属于org：

```
/orgs/{org_id}
/orgs/{org_id}/apps
/apps/{app_id}
/apps/{app_id}/dynos
/dynos/{dyno_id}
```
