# YuanShen
原神虚空终端配置文件
各项参数代表的意义请查阅官方wiki:https://wiki.metacubex.one/

本配置文件基于官方RULE-SET示例配置修改而来(2025.03.08)
改动如下：
将健康检查地址更换为Cloudflare，避免检查次数过多导致节点ip被Google风控
允许局域网连接关闭，不允许其他设备的流量经过Clash，路由/网关设备请将其改为true
将Clash控制面板更换为Zashboard，个人更喜欢Zashboard
私有域名，cn域名，bilibili域名，NTP域名及其他域名使用realip，改善兼容性
DoH指定subnet地址并强制覆盖，用以缓解CDN问题
阿里DoH强制开启HTTP/3，降低dns解析延迟
私有域名，cn域名，bilibili域名使用系统dns解析，解决局域网连接问题，最大程度使用各互联网平台的CDN，优化视频加载速度等
哔哩哔哩策略组默认直连
添加秋风广告规则，拦截常见广告SDK与服务器
删除biliintl_domain，ehentai_domain，pixiv_domain规则集
