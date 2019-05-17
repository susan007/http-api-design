##### 动作

首选不需要特殊操作的端点配置。在案件中如果需要操作，请使用“actions”前缀明确地将其删除：

```
/resources/:resource/actions/:action
```

e.g. to stop a particular run:

```
/runs/{run_id}/actions/stop
```

对集合的操作也应最小化。在需要的地方，他们应该使用顶级的动作来避免命名空间冲突并清楚地显示了操作范围：

```
/actions/:action/resources
```

e.g. to restart all servers:

```
/actions/restart/servers
```
