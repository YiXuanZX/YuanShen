# YuanShen
原神虚空终端配置文件

各项参数的注释请查阅官方wiki：https://wiki.metacubex.one/

本配置文件基于官方RULE-SET示例配置修改而来(2025.03.08)

# 改动如下：

将健康检查地址更换为Cloudflare，避免检查次数过多导致节点ip被Google风控

允许局域网连接关闭，不允许其他设备的流量经过Clash，路由/网关设备请将其改为true

将Clash控制面板更换为Zashboard，个人更喜欢Zashboard

局域网域名，cn域名，bilibili域名及其他域名(详见fakeip-filter规则集)使用realip，改善兼容性

局域网域名，cn域名，bilibili域名使用系统dns解析(即ISP下发dns)，解决局域网设备互联问题，优先使用离你地理位置最近的CDN，优化视频加载速度等

节点域名使用系统dns解析，用以适配多入口的机场

nameserver使用非加密的公共dns，若当地ISP的dns干扰不严重则没有使用加密dns的必要

哔哩哔哩策略组默认直连

局域网域名直连

添加秋风广告规则，拦截常见广告SDK域名(不建议使用anti等其他规则，文件过大，影响clash域名匹配效率)

删除没有使用的biliintl_domain，ehentai_domain，pixiv_domain规则集
