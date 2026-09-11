# MyClash

**越是常用越要细分，不常用只保证可用。**

## 配置文件

使用方法：复制链接，导入代理客户端

```txt
https://raw.githubusercontent.com/Mugzx/MyClash/main/Config/myclash.yaml
```

### 备注

> [!WARNING]
> - DNS配置和路由规则是配套的，非必要不要破坏正常分流
> - 规则为 `rule-set` 模式，使用 `domain` 与 `ipcidr` 格式，不引用 Geodata（避免臃肿）

## 介绍

### 内置策略组

- `默认代理`
- `自动选择`
- `负载均衡`
- `AI`
- `Discord`
- `FCM`
- `Games`
- `GitHub`
- `Google`
- `YouTube`
- `Microsoft`
- `PayPal`
- `Spotify`
- `Telegram`
- `X`
- `手动选择`
- `本地直连`
- `广告拦截`
- `漏网之鱼`

### 内置节点组

> - _所有组均为手动选择 (select)，内部包含对应的「自动选择」策略组和「负载均衡」策略组_

- `香港`
- `日本`
- `新加坡`
- `美利坚`

- _自动排除非国家或地区的信息节点_

- `低倍率节点`
- `高倍率节点`

> - 自动识别节点倍率，并分别归类为独立节点组：
>   - 高倍率节点（倍率 >1）
>   - 低倍率节点（倍率 ≤0.9）

- `其它节点`

> - _一般未匹配到地区组的节点节点将归类至 「其他节点」，最后回退到 REJECT_

## 致谢

感谢以下项目以及所有上游项目

- [YiXuanZX/rules](https://github.com/YiXuanZX/rules)
- [appshubcc/bett-rules](https://github.com/appshubcc/bett-rules)
- [217heidai/adblockfilters](https://github.com/217heidai/adblockfilters)
- [Koolson/Qure](https://github.com/Koolson/Qure)
- [AIsouler/MyClash](https://github.com/AIsouler/MyClash)
