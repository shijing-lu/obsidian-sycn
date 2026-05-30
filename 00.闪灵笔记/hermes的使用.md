> hermes 是一个 ai agent，功能和openclaw相似，但是具有持续自我迭代的功能。

进阶使用

[角色定义网站](https://github.com/msitarzewski/agency-agents)

多模型使用，主副模型切换使用

config.yaml 中搜索auxiliary

```
auxiliary:
  vision:
    provider: auto
    model: ''
    base_url: ''
    api_key: ''
    timeout: 120
    extra_body: {}
    download_timeout: 30
  web_extract:
    provider: auto
    model: ''
    base_url: ''
    api_key: ''
    timeout: 360
    extra_body: {}
  compression:
    provider: auto
    model: ''
    base_url: ''
    api_key: ''
    timeout: 120
    extra_body: {}
  session_search:
    provider: auto
    model: ''
    base_url: ''
    api_key: ''
    timeout: 30
    extra_body: {}
    max_concurrency: 3
  skills_hub:
    provider: auto
    model: ''
    base_url: ''
    api_key: ''
    timeout: 30
    extra_body: {}
  approval:
    provider: auto
    model: ''
    base_url: ''
    api_key: ''
    timeout: 30
    extra_body: {}
  mcp:
    provider: auto
    model: ''
    base_url: ''
    api_key: ''
    timeout: 30
    extra_body: {}
  title_generation:
    provider: auto
    model: ''
    base_url: ''
    api_key: ''
    timeout: 30
    extra_body: {}
  curator:
    provider: auto
    model: ''
    base_url: ''
    api_key: ''
    timeout: 600
    extra_body: {}

```

有 vision、 web_extract、compression、 session_search、skills_hub、approval、mcp、title_generation、curator
`` hermes dashboard``
![[PixPin_2026-05-06_10-23-20.png]]
可以在这里配置

查看log 看是否成功调用辅助模型

安装 webui，更好地聊天