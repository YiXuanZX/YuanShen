# YuanShen
原神虚空终端配置文件

各项参数的注释请查阅官方wiki：https://wiki.metacubex.one/

本配置文件基于官方RULE-SET示例配置修改而来(2025.03.08)

# 改动如下：

将健康检查地址更换为Cloudflare，避免短时间内检查次数过多导致节点ip被Google风控

关闭允许局域网连接，不允许其他设备的流量经过Clash核心，路由/网关设备请将其值改为true

将Clash控制面板更换为Zashboard，个人更喜欢Zashboard

跳过对私网域名，cn域名的嗅探

私网域名，cn域名及其他域名(详见fakeip-filter规则集)使用realip，改善兼容性

私网域名，cn域名使用系统dns解析(即ISP下发的dns)，解决局域网设备互联问题，最大程度使用离你地理位置最近的CDN，优化视频加载速度

节点域名使用系统dns解析，用以兼容多入口的机场

nameserver使用非加密的公共dns，若当地ISP的dns干扰不严重则没有使用加密dns的必要

哔哩哔哩策略组默认直连

私网域名直连

将非cn域名规则放在cn域名规则之前，解决国内公司的海外网站因主域名在cn域名列表里而被阻止访问的问题

添加秋风广告规则，拦截常见广告SDK域名(不建议使用anti等其他规则，规则数量过多，影响clash的规则匹配效率)

删除没有使用的biliintl_domain，ehentai_domain，pixiv_domain规则集
