AdGuard PCDN 屏蔽规则 (adguard-pcdn-rule)
这是一个专门为 AdGuard、PassWall、软路由及各平台广告拦截器设计的 PCDN (Peer-to-Peer CDN) 专项屏蔽列表。旨在斩断视频平台（优爱腾、B站、芒果等）及云服务商在后台私自占用用户上传带宽的行为。

🚀 项目特色
多源合一：深度整合 anti-AD、SMAdHosts、uselibrary、thhbdd 等多个权威 PCDN 拦截库。

物理去重：采用严格的物理去重算法，确保规则库无重复行，提升拦截效率，降低内存占用。

B站核心锁定：针对 Bilibili 的 PCDN 调度规则进行了专项锁定和追补，确保在拦截 P2P 的同时不影响正常的视频加载。

全平台覆盖：不仅适用于网页端，还针对智能电视 (OTT)、手机 APP 及 PC 客户端的 PCDN 行为进行了针对性补吸。

格式纯净：严格遵守 AdGuard 标准语法，不做冗余的通配符合并，保持规则的原始拦截逻辑。

📂 包含分类
Bilibili 专项 (核心锁定)

主流视频平台 (网易、咪咕、爱奇艺、优酷、芒果、搜狐、乐视等)

直播与下载工具 (迅雷、YY、暴风、龙珠、熊猫、花椒、PPTV等)

云服务商 P2P 接口 (阿里云、百度云、腾讯云、京东云、华为云、金山云等)

专业 PCDN 服务商 (星域云、网心云、世纪互联、博纳云等)

音频与其它 (喜马拉雅、蜻蜓FM等)

🛠️ 如何使用
1. AdGuard / AdGuard Home
直接添加以下订阅地址：
https://raw.githubusercontent.com/zhecydn/adguard-pcdn-rule/main/pcdn.txt

2. PassWall / OpenWrt
如果你需要纯域名格式用于软路由屏蔽，可以参考本项目提取的域名逻辑，将其直接填入“黑名单”或“屏蔽列表”中。

⚠️ 补充说明
关于 WebRTC：建议配合浏览器的 WebRTC Control 以及adguard相关插件使用，效果更佳。

业务回退机制：本规则拦截的是 P2P 调度域名。拦截成功后，播放器会自动回退到正常的 CDN 直连模式，不会影响视频观看，但会显著降低上传带宽占用。

🤝 鸣谢来源
感谢以下项目提供的原始规则支持（排名不分先后）：

[anti-AD](https://github.com/privacy-protection-tools/anti-AD)

[SM-Ad-FuckU-hosts](https://www.google.com/search?q=https://github.com/2Gardon/SM-Ad-FuckU-hosts)

[uselibrary/PCDN](https://www.google.com/search?q=https://github.com/uselibrary/PCDN)

[thhbdd/Block-pcdn-domains](https://www.google.com/search?q=https://github.com/thhbdd/Block-pcdn-domains)
