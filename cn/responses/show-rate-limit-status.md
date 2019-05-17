#### 显示速率限制状态

来自客户的速率限制请求，以保护服务的健康
并为其他客户保持高服务质量。 
参考以下内容[token bucket algorithm](http://en.wikipedia.org/wiki/Token_bucket) 去量化请求限制

在每个请求中返回剩余的请求令牌数`RateLimit-Remaining`响应头。相关阅读[会话令牌](https://www.ibm.com/support/knowledgecenter/zh/SSPH29_9.0.1/com.ibm.help.common.infocenter.aps/PowerTools/TokenAnalyzer/c_WhatareSessionTokens001.html)
