# HTTP API 设计指导


本指南描述了一组HTTP + JSON API设计实践， 
源自工作实践中提取出来 [Heroku Platform API](https://devcenter.heroku.com/articles/platform-api-reference).


本指南通知该API的附加内容，并指导新内部Heroku的API。我们希望API设计师也对它感兴趣Heroku之外。


我们的目标是一致性，专注于业务逻辑，同时避免设计轮子。
我们正在寻找一种良好，一致，记录良好的方式来设计API，而不一定是唯一/理想的方式。

我们假设您熟悉HTTP + JSON API的基础知识，并不会涵盖本指南中所有基础知识。

可在线阅读和多种格式 [gitbook](https://www.gitbook.com/read/book/geemus/http-api-design).

欢迎捐赠 [contributions](../CONTRIBUTING.md)

目录 [Summary](SUMMARY.md)

### 翻译
 * [Portuguese version](https://github.com/Gutem/http-api-design/) (based on [fba98f08b5](https://github.com/interagent/http-api-design/commit/fba98f08b50acbb08b7b30c012a6d0ca795e29ee)), by [@Gutem](https://github.com/Gutem/)
 * [Spanish version](https://github.com/jmnavarro/http-api-design) (based on [2a74f45](https://github.com/interagent/http-api-design/commit/2a74f45b9afaf6c951352f36c3a4e1b0418ed10b)), by [@jmnavarro](https://github.com/jmnavarro/)
 * [Korean version](https://github.com/yoondo/http-api-design) (based on [f38dba6](https://github.com/interagent/http-api-design/commit/f38dba6fd8e2b229ab3f09cd84a8828987188863)), by [@yoondo](https://github.com/yoondo/)
 * [Simplified Chinese version](https://github.com/ZhangBohan/http-api-design-ZH_CN) (based on [337c4a0](https://github.com/interagent/http-api-design/commit/337c4a05ad08f25c5e232a72638f063925f3228a)), by [@ZhangBohan](https://github.com/ZhangBohan/)
 * [Traditional Chinese version](https://github.com/kcyeu/http-api-design) (based on [232f8dc](https://github.com/interagent/http-api-design/commit/232f8dc6a941d0b25136bf64998242dae5575f66)), by [@kcyeu](https://github.com/kcyeu/)
 * [Turkish version](https://github.com/hkulekci/http-api-design/tree/master/tr) (based on [c03842f](https://github.com/interagent/http-api-design/commit/c03842fda80261e82860f6dc7e5ccb2b5d394d51)), by [@hkulekci](https://github.com/hkulekci/)

