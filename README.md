# MyClash

## 配置文件

使用方法：复制链接，导入代理客户端

```txt
https://github.com/Mugzx/MyClash/raw/main/Config/myclash.yaml
```

### 备注

> [!WARNING]
> - DNS配置和路由规则是配套的，非必要不要破坏正常分流
> - 规则为 `rule-set` 模式，使用 `domain` 与 `ipcidr` 格式，不引用 Geodata（避免臃肿）
> - 一些较为复杂的网络情况下，`geolocation-cn` 可能分流不完全，可以改用 `cn_additional`

「IPv6」：在 [4f29c75](https://github.com/Mugzx/MyClash/commit/4f29c75) 里去掉了相关的开启字段（应该根据情况手动开启）。

## 介绍

- 自动排除非国家或地区的信息节点
- 自动识别节点倍率，并分别归类为独立节点组：
  - 高倍率节点（倍率 >1）
  - 低倍率节点（倍率 ≤0.9）
- 无该地区节点的策略组将回退到 REJECT

## 内置策略组

- `默认代理`
- `自动选择`
- `负载均衡`
- `AI`
- `FCM`
- `Games` (Steam+Xbox)
- `GitHub`
- `Google`
- `Media` (YouTube+TikTok+Twitch)
- `Microsoft`
- `Telegram`
- `X`
- `手动选择`
- `本地直连`
- `广告拦截`
- `漏网之鱼`

## 内置节点组

> - _所有组均为手动选择 (select)，内部包含对应的自动选择策略组和负载均衡策略组_
> - _未匹配到地区组的节点节点将归类至 「其他节点」_

- `香港`
- `日本`
- `美国`
- `新加坡`
- `台湾省`
- `低倍率节点`
- `高倍率节点`
- `其他节点`

## 致谢

感谢以下项目以及所有上游项目

- [YiXuanZX/rules](https://github.com/YiXuanZX/rules)
- [MetaCubeX/meta-rules-dat](https://github.com/MetaCubeX/meta-rules-dat)
- [wwqgtxx/clash-rules](https://github.com/wwqgtxx/clash-rules)
- [217heidai/adblockfilters](https://github.com/217heidai/adblockfilters)
- [Koolson/Qure](https://github.com/Koolson/Qure)
- [AIsouler/MyClash](https://github.com/AIsouler/MyClash)
