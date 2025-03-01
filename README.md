默认ip192.168.100.1 密码password R68S刷入方式： dd if=/tmp/upload/aaa.img of=/dev/mmcblk0
教程 https://www.bilibili.com/video/BV1Rr4y1L7kx/

**English** | [中文](https://p3terx.com/archives/build-openwrt-with-github-actions.html)

# Actions-OpenWrt

[![LICENSE](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square&label=LICENSE)](https://github.com/P3TERX/Actions-OpenWrt/blob/master/LICENSE)
![GitHub Stars](https://img.shields.io/github/stars/P3TERX/Actions-OpenWrt.svg?style=flat-square&label=Stars&logo=github)
![GitHub Forks](https://img.shields.io/github/forks/P3TERX/Actions-OpenWrt.svg?style=flat-square&label=Forks&logo=github)

A template for building OpenWrt with GitHub Actions

## Usage

- Click the [Use this template](https://github.com/P3TERX/Actions-OpenWrt/generate) button to create a new repository.
- Generate `.config` files using [Lean's OpenWrt](https://github.com/coolsnowwolf/lede) source code. ( You can change it through environment variables in the workflow file. )
- Push `.config` file to the GitHub repository.
- Select `Build OpenWrt` on the Actions page.
- Click the `Run workflow` button.
- When the build is complete, click the `Artifacts` button in the upper right corner of the Actions page to download the binaries.

## Tips

- It may take a long time to create a `.config` file and build the OpenWrt firmware. Thus, before create repository to build your own firmware, you may check out if others have already built it which meet your needs by simply [search `Actions-Openwrt` in GitHub](https://github.com/search?q=Actions-openwrt).
- Add some meta info of your built firmware (such as firmware architecture and installed packages) to your repository introduction, this will save others' time.

## Credits

- [Microsoft Azure](https://azure.microsoft.com)
- [GitHub Actions](https://github.com/features/actions)
- [OpenWrt](https://github.com/openwrt/openwrt)
- [Lean's OpenWrt](https://github.com/coolsnowwolf/lede)
- [tmate](https://github.com/tmate-io/tmate)
- [mxschmitt/action-tmate](https://github.com/mxschmitt/action-tmate)
- [csexton/debugger-action](https://github.com/csexton/debugger-action)
- [Cowtransfer](https://cowtransfer.com)
- [WeTransfer](https://wetransfer.com/)
- [Mikubill/transfer](https://github.com/Mikubill/transfer)
- [softprops/action-gh-release](https://github.com/softprops/action-gh-release)
- [ActionsRML/delete-workflow-runs](https://github.com/ActionsRML/delete-workflow-runs)
- [dev-drprasad/delete-older-releases](https://github.com/dev-drprasad/delete-older-releases)
- [peter-evans/repository-dispatch](https://github.com/peter-evans/repository-dispatch)


https://www.right.com.cn/forum/thread-3682029-1-1.html
OpenWrt 编译 LuCI ---> Applications 添加插件应用说明 【人人为我，我为人人】   2021.11.18 更新 ！！！

make menuconfig  进入定制界面
进入编译选项配置界面,.按照需要配置.( ‘*’ 代表编入固件，‘M’ 表示编译成模块或者IPK包， ‘空’不编译 )

非常感谢大佬”L有大雕“更正补充，20181121
大佬源码仓库：https://github.com/coolsnowwolf/lede
内容仅供参考，请根据个人实际情况使用，如果出现问题则后果自负。


选择LuCI 配置 添加插件应用：常用
-----------------------------------------------------------------------------------------
LuCI ---> Applications ---> luci-app-accesscontrol  #访问时间控制
LuCI ---> Applications ---> luci-app-adbyby-plus   #广告屏蔽大师Plus +
LuCI ---> Applications ---> luci-app-arpbind  #IP/MAC绑定
LuCI ---> Applications ---> luci-app-autoreboot  #支持计划重启
LuCI ---> Applications ---> luci-app-ddns   #动态域名 DNS（集成阿里DDNS客户端）
LuCI ---> Applications ---> luci-app-filetransfer  #文件传输（可web安装ipk包）
LuCI ---> Applications ---> luci-app-firewall   #添加防火墙
LuCI ---> Applications ---> luci-app-frpc   #内网穿透 Frp
LuCI ---> Applications ---> luci-app-ipsec-vpnd  #VPN服务器 IPSec
LuCI ---> Applications ---> luci-app-nlbwmon   #网络带宽监视器
LuCI ---> Applications ---> luci-app-ramfree  #释放内存
LuCI ---> Applications ---> luci-app-samba   #网络共享（Samba）
-------------------------------------------------------------------------------------------
LuCI ---> Applications ---> luci-app-ssr-plus   #SSR科学上网Plus+
    luci-app-ssr-plus ---> Include Shadowsocks Libev Client  #SS Libev客户端(轻量级)
    luci-app-ssr-plus ---> Include Shadowsocks Libev Server  #SS Libev服务端(轻量级)
    luci-app-ssr-plus ---> Include ShadowsocksR Libev Client  #SSR Libev客户端(轻量级)
    luci-app-ssr-plus ---> Include ShadowsocksR Libev Server  #SSR Libev服务端(轻量级)
    luci-app-ssr-plus ---> Include Include Shadowsocks Simple Obfs Plugin  #SS Simple-Obfs混淆代理(Nginx)
    luci-app-ssr-plus ---> Include Xray  #Xray代理(XTLS)
-------------------------------------------------------------------------------------------
LuCI ---> Applications ---> luci-app-turboacc   #Turbo ACC 网络加速(支持 Fast Path 或者 硬件 NAT)
LuCI ---> Applications ---> luci-app-unblockmusic  #解锁网易云灰色歌曲3合1新版本
LuCI ---> Applications ---> luci-app-upnp   #通用即插即用UPnP（端口自动转发）
LuCI ---> Applications ---> luci-app-vlmcsd  #KMS服务器设置
LuCI ---> Applications ---> luci-app-vsftpd  #FTP服务器
LuCI ---> Applications ---> luci-app-wifischedule  #WiFi 计划
LuCI ---> Applications ---> luci-app-wireless-regdb  #WiFi无线
LuCI ---> Applications ---> luci-app-wol   #WOL网络唤醒
LuCI ---> Applications ---> luci-app-xlnetacc  #迅雷快鸟
LuCI ---> Applications ---> luci-app-zerotier  #ZeroTier内网穿透



以下是全部：           注：应用后面标记 “ * ” 为最近新添加；标记“ ! ”与其他插件依赖或冲突。
-------------------------------------------------------------------------------------------------------------------
LuCI ---> Applications ---> luci-app-accesscontrol  #访问时间控制
LuCI ---> Applications ---> luci-app-acme  #ACME自动化证书管理环境（丢弃）
LuCI ---> Applications ---> luci-app-adblock   #ADB广告过滤
LuCI ---> Applications ---> luci-app-adbyby-plus  #广告屏蔽大师Plus +
LuCI ---> Applications ---> luci-app-adbyby   #广告过滤大师（丢弃）
LuCI ---> Applications ---> luci-app-adguardhome  #AdGuard home广告过滤（Le库以外的插件）
LuCI ---> Applications ---> luci-app-adkill   #广告过滤（丢弃）
LuCI ---> Applications ---> luci-app-advanced-reboot  #Linksys高级重启
LuCI ---> Applications ---> luci-app-advancedsetting  #系统高级设置（Le库以外的插件）
LuCI ---> Applications ---> luci-app-ahcp  #Ad-Hoc配置协议(AHCP) ipv6 and 双栈 自动配置协议 !
LuCI ---> Applications ---> luci-app-airplay2   #Apple AirPlay2 无损音频接收服务器
LuCI ---> Applications ---> luci-app-aliddns   #阿里DDNS客户端（丢弃，集成至ddns）
LuCI ---> Applications ---> luci-app-aliyundrive-webdav  #阿里云盘 WebDAV 服务
LuCI ---> Applications ---> luci-app-amule  #aMule下载工具 !
LuCI ---> Applications ---> luci-app-argon-config  #Argon主题配置插件（Le库以外的插件）
LuCI ---> Applications ---> luci-app-aria2 # Aria2下载工具
LuCI ---> Applications ---> luci-app-arpbind  #IP/MAC绑定
LuCI ---> Applications ---> luci-app-asterisk  #支持Asterisk电话服务器
LuCI ---> Applications ---> luci-app-attendedsysupgrade  #固件更新升级相关
LuCI ---> Applications ---> luci-app-autoreboot  #支持计划重启
LuCI ---> Applications ---> luci-app-baidupcs-web  #百度网盘管理
LuCI ---> Applications ---> luci-app-bcp38  #BCP38网络入口过滤（不确定）
LuCI ---> Applications ---> luci-app-bird1-ipv4  #对Bird1-ipv4的支持
LuCI ---> Applications ---> luci-app-bird1-ipv6  #对Bird1-ipv6的支持
LuCI ---> Applications ---> luci-app-bird4   #Bird 4（未知）（丢弃）
LuCI ---> Applications ---> luci-app-bird6   #Bird 6（未知）（丢弃）
LuCI ---> Applications ---> luci-app-bmx6  #BMX6路由协议
LuCI ---> Applications ---> luci-app-bmx7  #BMX7路由协议（丢弃）
LuCI ---> Applications ---> luci-app-caldav  #联系人（丢弃）
LuCI ---> Applications ---> luci-app-cifs-mount   #CIFS/SMB挂载设置
LuCI ---> Applications ---> luci-app-cifsd  #CIFS/SMB网络共享
LuCI ---> Applications ---> luci-app-cjdns  #加密IPV6网络相关
LuCI ---> Applications ---> luci-app-clamav  #ClamAV杀毒软件
LuCI ---> Applications ---> luci-app-clash  #Clash客户端（Le库以外的插件）
LuCI ---> Applications ---> luci-app-commands  #Shell命令模块
LuCI ---> Applications ---> luci-app-cshark  #CloudShark捕获工具
LuCI ---> Applications ---> luci-app-dawn  #分布式AP管理程序
LuCI ---> Applications ---> luci-app-ddns   #动态域名 DNS（集成阿里DDNS客户端）
LuCI ---> Applications ---> luci-app-diag-core   #core诊断工具
LuCI ---> Applications ---> luci-app-diskman   #磁盘管理工具
    luci-app-diskman ---> Include btrfs-progs   #新型的写时复制 (COW)
    luci-app-diskman ---> Include lsblk   #lsblk命令 用于列出所有可用块设备的信息
    luci-app-diskman ---> Include mdadm   #mdadm命令 用于创建、管理、监控RAID设备的工具
    luci-app-diskman ---> Include kmod-md-raid456   #RAID 4,5,6 驱动程序模块（丢弃）
    luci-app-diskman ---> Include kmod-md-linear   #RAID 驱动程序模块（丢弃）
LuCI ---> Applications ---> luci-app-dnscrypt-proxy  #DNSCrypt解决DNS污染
LuCI ---> Applications ---> luci-app-dnsfilter  #DNSFilter基于DNS的广告过滤
LuCI ---> Applications ---> luci-app-dnsforwarder  #DNSForwarder防DNS污染
LuCI ---> Applications ---> luci-app-dnspod  #DNSPod动态域名解析（丢弃）
LuCI ---> Applications ---> luci-app-docker  #Docker容器(dockerman更名为docker)
LuCI ---> Applications ---> luci-app-dump1090  #民航无线频率（不确定）
LuCI ---> Applications ---> luci-app-dynapoint  #DynaPoint（未知）
LuCI ---> Applications ---> luci-app-e2guardian   #Web内容过滤器
LuCI ---> Applications ---> luci-app-easymesh   #简单MESH(可有线+无线回程)
LuCI ---> Applications ---> luci-app-eqos  #基于IP地址限速（Le库以外的插件）
LuCI ---> Applications ---> luci-app-familycloud   #家庭云盘
LuCI ---> Applications ---> luci-app-fileassistant   #文件管理助手（Le库以外的插件）
LuCI ---> Applications ---> luci-app-filetransfer  #文件传输（可web安装ipk包）
LuCI ---> Applications ---> luci-app-firewall   #添加防火墙
LuCI ---> Applications ---> luci-app-flowoffload  #Turbo ACC网络加速（集成FLOW,BBR,NAT,DNS（丢弃，移至TurboACC）
LuCI ---> Applications ---> luci-app-freifunk-diagnostics   #freifunk组件 诊断（未知）（丢弃）
LuCI ---> Applications ---> luci-app-freifunk-policyrouting  #freifunk组件 策略路由（未知）（丢弃）
LuCI ---> Applications ---> luci-app-freifunk-widgets  #freifunk组件 索引（未知）（丢弃）
LuCI ---> Applications ---> luci-app-frpc   #内网穿透Frp客户端
LuCI ---> Applications ---> luci-app-frps   #内网穿透Frp服务端
LuCI ---> Applications ---> luci-app-fwknopd  #Firewall Knock Operator服务器
LuCI ---> Applications ---> luci-app-guest-wifi   #WiFi访客网络
LuCI ---> Applications ---> luci-app-gfwlist   #GFW域名列表（丢弃）
LuCI ---> Applications ---> luci-app-go-aliyundrive-webdav   #阿里云盘webdav协议(文件管理/同步等)  *
LuCI ---> Applications ---> luci-app-gost  #隐蔽的https代理（Le库以外的插件）
LuCI ---> Applications ---> luci-app-haproxy-tcp   #HAProxy负载均衡-TCP
LuCI ---> Applications ---> luci-app-hd-idle  #硬盘休眠
LuCI ---> Applications ---> luci-app-hnet  #Homenet Status家庭网络控制协议
LuCI ---> Applications ---> luci-app-https-dns-proxy  #通过HTTPS代理为DNS提供Web UI
LuCI ---> Applications ---> luci-app-ipsec-vpnd  #VPN服务器 IPSec
LuCI ---> Applications ---> luci-app-jd-dailybonus  #京东签到服务
LuCI ---> Applications ---> luci-app-kodexplorer  #KOD可道云私人网盘（与vnStat冲突 ! ）
LuCI ---> Applications ---> luci-app-kooldns  #VPN服务器 ddns替代方案（丢弃）
LuCI ---> Applications ---> luci-app-koolproxy  #KP去广告（丢弃）
LuCI ---> Applications ---> luci-app-lxc   #LXC容器管理
LuCI ---> Applications ---> luci-app-meshwizard #网络设置向导（丢弃）
LuCI ---> Applications ---> luci-app-minidlna   #完全兼容DLNA / UPnP-AV客户端的服务器软件
LuCI ---> Applications ---> luci-app-mjpg-streamer   #兼容Linux-UVC的摄像头程序
LuCI ---> Applications ---> luci-app-mtwifi  #MTWiFi驱动的支持 （丢弃）
LuCI ---> Applications ---> luci-app-mmc-over-gpio   #添加SD卡操作界面（丢弃）
LuCI ---> Applications ---> luci-app-multiwan   #多拨虚拟网卡（丢弃，移至syncdial）
LuCI ---> Applications ---> luci-app-mwan   #MWAN负载均衡（丢弃）
LuCI ---> Applications ---> luci-app-music-remote-center   #PCHiFi 数字转盘遥控
LuCI ---> Applications ---> luci-app-mwan3   #MWAN3负载均衡
LuCI ---> Applications ---> luci-app-mwan3helper   #MWAN3分流助手
LuCI ---> Applications ---> luci-app-n2n_v2   #N2N内网穿透 N2N v2 VPN服务
LuCI ---> Applications ---> luci-app-netdata  #Netdata实时监控（图形化）
LuCI ---> Applications ---> luci-app-nfs   #NFS网络共享
LuCI ---> Applications ---> luci-app-nft-qos  #QOS流控 Nftables版
LuCI ---> Applications ---> luci-app-ngrokc  #Ngrok 内网穿透（丢弃）
LuCI ---> Applications ---> luci-app-nlbwmon   #网络带宽监视器
LuCI ---> Applications ---> luci-app-noddos  #NodDOS Clients 阻止DDoS攻击
LuCI ---> Applications ---> luci-app-nps   #内网穿透nps
LuCI ---> Applications ---> luci-app-ntpc   #NTP时间同步服务器
LuCI ---> Applications ---> luci-app-ocserv  #OpenConnect VPN服务
LuCI ---> Applications ---> luci-app-olsr  #OLSR配置和状态模块
LuCI ---> Applications ---> luci-app-olsr-services  #OLSR服务器
LuCI ---> Applications ---> luci-app-olsr-viz   #OLSR可视化
LuCI ---> Applications ---> luci-app-ocserv   #OpenConnect VPN服务（丢弃）
LuCI ---> Applications ---> luci-app-openclash  #运行在OpenWrt上的Clash代理客户端（Le库以外的插件）
LuCI ---> Applications ---> luci-app-openvpn  #OpenVPN客户端
LuCI ---> Applications ---> luci-app-openvpn-server  #易于使用的OpenVPN服务器 Web-UI
LuCI ---> Applications ---> luci-app-oscam   #OSCAM服务器（丢弃）
LuCI ---> Applications ---> luci-app-p910nd   #打印服务器模块
LuCI ---> Applications ---> luci-app-pagekitec   #Pagekitec内网穿透客户端
LuCI ---> Applications ---> luci-app-passwall  #科学上网（Li大佬插件）
    Configuration ---> Include Brook  #Brook代理(跨平台强加密且不可检测代理)
    Configuration ---> Include ChinaDNS-NG  #防污染DNS服务
    Configuration ---> Include Haproxy  #HAProxy  #HAProxy负载均衡
    Configuration ---> Include Hysteria  #Hysteria双边加速工具
    Configuration ---> Include Kcptun  #Kcptun双边加速工具
    Configuration ---> Include NaiveProxy  #NaiveProxy代理(Chrome网络堆栈伪装流量)
    Configuration ---> Include PDNSD  #DNS服务器
    Configuration ---> Include Shadowsocks Libev Client  #SS Libev客户端(轻量级)
    Configuration ---> Include Shadowsocks Libev Server  #SS Libev服务端(轻量级)
    Configuration ---> Include Shadowsocks Rust Client  #SS Rust客户端(负载均衡/探测延迟)
    Configuration ---> Include ShadowsocksR Libev Client  #SSR Libev客户端(轻量级)
    Configuration ---> Include ShadowsocksR Libev Server  #SSR Libev服务端(轻量级)
    Configuration ---> Include Simple-Obfs (Shadowsocks plugin)  #simple-Obfs简单混淆工具(Nginx)
    Configuration ---> Include Trojan_GO  #Trojan_GO代理(直接模仿协议HTTPS)
    Configuration ---> Include Trojan_Plus  #Trojan_Plus代理(直接模仿协议HTTPS)
    Configuration ---> Include V2ray  #V2Ray代理
    Configuration ---> Include v2ray-plugin (Shadowsocks plugin)  #SS V2ray插件(WebSocket+TLS )
    Configuration ---> Include Xray  #Xray代理(XTLS)
    Configuration ---> Include Xray-Plugin (Shadowsocks Plugin)  #SS Xray插件(WebSocket+TLS )   *
    Configuration ---> Include Dns2socks  #DNS服务器（丢弃）
    Configuration ---> Include Redsocks2  #Redsocks2代理(透明TCP定向Socks/HTTPS代理服务器)（丢弃）
    Configuration ---> Include Shadowsocks  #SS代理（丢弃）
    Configuration ---> Include Shadowsocks Server  #SS服务器（丢弃）
    Configuration ---> Include Shadowsocks Rust (AEAD ciphers only)  #SS-RUST代理(AEAD加密)（丢弃）
    Configuration ---> Include ShadowsocksR   #SSR代理（丢弃）
    Configuration ---> Include ShadowsocksR Server  #SSR服务器（丢弃）
    Configuration ---> Include Https DNS Proxy(DoH)  #HttpsDNS服务（丢弃）
LuCI ---> Applications ---> luci-app-polipo  #Polipo代理(是一个小型且快速的网页缓存代理)
LuCI ---> Applications ---> luci-app-pppoe-relay  #PPPoE NAT穿透 点对点协议（PPP）
LuCI ---> Applications ---> luci-app-pptp-server  #VPN服务器 PPTP
LuCI ---> Applications ---> luci-app-privoxy  #Privoxy网络代理(带过滤无缓存)
LuCI ---> Applications ---> luci-app-ps3netsrv  #PS3 NET服务器(用于加载蓝光/游戏ISO/PKG)
LuCI ---> Applications ---> luci-app-pushbot  #全能推送(钉钉推送,企业微信推送,Bark,PushPlus推送)
LuCI ---> Applications ---> luci-app-qbittorrent  #BT下载工具(qBittorrent)
    Build Version Selection (Static Build)  ---> Static Build  #选择静态编译版本
    Build Version Selection (Static Build)  ---> Dynamic Build  #选择动态编译版本
LuCI ---> Applications ---> luci-app-qos   #流量服务质量(QoS)流控
LuCI ---> Applications ---> luci-app-radicale   #CalDAV/CardDAV同步工具
LuCI ---> Applications ---> luci-app-ramfree  #释放内存
LuCI ---> Applications ---> luci-app-rclone  #命令行云端同步工具
    Include rclone-webui  #Rclone界面
    Include rclone-ng (another webui)  #Rclone另一个界面
    Include fuse-utils (mount cloud storage)  #fuse-utils（挂载云存储）（丢弃）
LuCI ---> Applications ---> luci-app-rp-pppoe-server  #Roaring Penguin PPPoE Server 服务器
LuCI ---> Applications ---> luci-app-samba   #网络共享（Samba）
LuCI ---> Applications ---> luci-app-samba4   #网络共享（Samba4）
LuCI ---> Applications ---> luci-app-serverchan   #微信/Telegram推送的插件
LuCI ---> Applications ---> luci-app-sfe  #Turbo ACC网络加速（丢弃，移至TurboACC）
LuCI ---> Applications ---> luci-app-shadowsocks   #SS科学上网（丢弃）
LuCI ---> Applications ---> luci-app-shadowsocks-libes  #SS-libev服务端
LuCI ---> Applications ---> luci-app-shairplay  #支持AirPlay功能
LuCI ---> Applications ---> luci-app-siitwizard  #SIIT配置向导  SIIT-Wizzard
LuCI ---> Applications ---> luci-app-simple-adblock  #简单的广告拦截
LuCI ---> Applications ---> luci-app-smartdns  #SmartDNS本地服务器（丢弃）
LuCI ---> Applications ---> luci-app-softethervpn  #SoftEther VPN服务器  NAT穿透
LuCI ---> Applications ---> luci-app-splash  #Client-Splash是无线MESH网络的一个热点认证系统
LuCI ---> Applications ---> luci-app-sqm  #流量智能队列管理（QOS）
LuCI ---> Applications ---> luci-app-squid   #Squid代理服务器
LuCI ---> Applications ---> luci-app-ssr-plus   #SSR科学上网Plus+（Le大佬插件）
    Include libustream-ssl  ---> Include libustream-wolfssl  #选择wolfSSL库(传输层安全协议)
    Include libustream-ssl  ---> Include libustream-openssl  #选择OpenSSL库(传输层安全协议)
    luci-app-ssr-plus ---> Include Kcptun  #Kcptun双边加速工具
    luci-app-ssr-plus ---> Include NaiveProxy  #NaiveProxy代理(Chrome网络堆栈伪装流量)
    luci-app-ssr-plus ---> Include Redsocks2  #Redsocks2代理(透明TCP定向Socks/HTTPS代理服务器)
    luci-app-ssr-plus ---> Include Shadowsocks Libev Client  #SS Libev客户端(轻量级)
    luci-app-ssr-plus ---> Include Shadowsocks Libev Server  #SS Libev服务端(轻量级)
    luci-app-ssr-plus ---> Include Shadowsocks Rust Client  #SS Rust客户端(负载均衡/探测延迟)
    luci-app-ssr-plus ---> Include Shadowsocks Rust Server  #SS Rust服务端(负载均衡/探测延迟)
    luci-app-ssr-plus ---> Include ShadowsocksR Libev Client  #SSR Libev客户端(轻量级)
    luci-app-ssr-plus ---> Include ShadowsocksR Libev Server  #SSR Libev服务端(轻量级)
    luci-app-ssr-plus ---> Include Simple-Obfs Plugin  #SS Simple-Obfs混淆代理(Nginx)
    luci-app-ssr-plus ---> Include Trojan  #Trojan代理(直接模仿协议HTTPS)
    luci-app-ssr-plus ---> Include Shadowsocks V2ray Plugin  #SS V2ray代理(WebSocket+TLS )
    luci-app-ssr-plus ---> Include Xray  #Xray代理(XTLS)
    luci-app-ssr-plus ---> Include Shadowsocks New Version  #新SS代理（丢弃）
    luci-app-ssr-plus ---> Include Shadowsocks  #SS代理（丢弃）
    luci-app-ssr-plus ---> Include Shadowsocks Rust (AEAD ciphers only)  #SS-RUST代理(AEAD密码)  （丢弃）
    luci-app-ssr-plus ---> Include V2ray  #V2Ray代理（丢弃）
    luci-app-ssr-plus ---> Include Xray (V2RAY/Trojan-GO implemented)  #Xray代理（丢弃）
    luci-app-ssr-plus ---> Include Trojan-go  #Trojan-go代理（丢弃）
    luci-app-ssr-plus ---> Include Shadowsocks Server  #SS服务器（丢弃）
    luci-app-ssr-plus ---> Include Shadowsocks Rust Server  #SS Rust服务器（丢弃）
    luci-app-ssr-plus ---> Include ShadowsocksR Server  #SSR服务器（丢弃）
    luci-app-ssr-plus ---> Include DNS2SOCKS  #DNS服务器（丢弃）
    luci-app-ssr-plus ---> Include ShadowsocksR Socks and Tunnel（丢弃）
    luci-app-ssr-plus ---> Include Socks Server  #socks代理服务器（丢弃）
LuCI ---> Applications ---> luci-app-ssr-pro  #SSR-Pro（丢弃）
LuCI ---> Applications ---> luci-app-ssrserver-python  #ShadowsocksR Python服务器
LuCI ---> Applications ---> luci-app-statistics  #流量监控工具
LuCI ---> Applications ---> luci-app-syncdial  #多拨虚拟网卡（原macvlan）
LuCI ---> Applications ---> luci-app-tinyproxy  #Tinyproxy是 HTTP(S)代理服务器
LuCI ---> Applications ---> luci-app-transmission   #BT下载工具
LuCI ---> Applications ---> luci-app-travelmate  #旅行路由器
LuCI ---> Applications ---> luci-app-ttyd   #网页终端命令行
LuCI ---> Applications ---> luci-app-turboacc   #Turbo ACC 网络加速(支持 Fast Path 或者 硬件 NAT)
    luci-app-turboacc ---> Include Shortcut-FE  #Shortcut-FE 流量分载
    luci-app-turboacc ---> Include BBR CCA  #BBR拥塞控制算法提升TCP网络性能
    luci-app-turboacc ---> Include DNSForwarder  #DNS防污染 Forwarder
    luci-app-turboacc ---> Include DNSProxy  #DNS防污染 Proxy
LuCI ---> Applications ---> luci-app-udpxy  #udpxy做组播服务器
LuCI ---> Applications ---> luci-app-uhttpd  #uHTTPd Web服务器
LuCI ---> Applications ---> luci-app-unblockmusic  #解锁网易云灰色歌曲3合1新版本
    UnblockNeteaseMusic Golang Version  #Golang版本
    UnblockNeteaseMusic NodeJS Version  #NodeJS版本
LuCI ---> Applications ---> luci-app-unblockneteasemusic-go  #解除网易云音乐（合并）
LuCI ---> Applications ---> luci-app-unblockneteasemusic-mini  #解除网易云音乐（合并）
LuCI ---> Applications ---> luci-app-unbound  #Unbound DNS解析器
LuCI ---> Applications ---> luci-app-upnp   #通用即插即用UPnP（端口自动转发）
LuCI ---> Applications ---> luci-app-usb-printer  #USB 打印服务器
LuCI ---> Applications ---> luci-app-uugamebooster  #UU网游加速器
LuCI ---> Applications ---> luci-app-v2ray-server   #V2Ray 服务器
LuCI ---> Applications ---> luci-app-v2ray-pro  #V2Ray透明代理（丢弃，集成SSR）
LuCI ---> Applications ---> luci-app-verysync  #微力同步
LuCI ---> Applications ---> luci-app-vlmcsd  #KMS服务器设置
LuCI ---> Applications ---> luci-app-vnstat   #vnStat网络监控（图表）（与kodexplorer冲突 ! ）
LuCI ---> Applications ---> luci-app-vpnbypass  #VPN BypassWebUI  绕过VPN设置
LuCI ---> Applications ---> luci-app-vsftpd  #FTP服务器
LuCI ---> Applications ---> luci-app-vssr  #VSSR科学上网（je大佬插件）
    luci-app-vssr ---> Include Xray  #Xray代理(XTLS)
    luci-app-vssr ---> Include Trojan  #Trojan代理(直接模仿协议HTTPS)
    luci-app-vssr ---> Include Kcptun  #Kcptun双边加速工具
    luci-app-vssr ---> Include Shadowsocks Xray Plugin  #SS Xray代理
    luci-app-vssr ---> Include ShadowsocksR Libev Server  #SSR Libev服务端(轻量级)
LuCI ---> Applications ---> luci-app-watchcat  #断网检测功能与定时重启
LuCI ---> Applications ---> luci-app-webadmin  #Web管理页面设置
LuCI ---> Applications ---> luci-app-webshell  #网页命令行终端（丢弃）
LuCI ---> Applications ---> luci-app-wifischedule  #WiFi 计划
LuCI ---> Applications ---> luci-app-wireguard  #VPN服务器 WireGuard状态
LuCI ---> Applications ---> luci-app-wireless-regdb  #WiFi无线
LuCI ---> Applications ---> luci-app-wol   #WOL网络唤醒
LuCI ---> Applications ---> luci-app-wrtbwmon  #实时流量监测
LuCI ---> Applications ---> luci-app-xlnetacc  #迅雷快鸟
LuCI ---> Applications ---> luci-app-zerotier  #ZeroTier内网穿透
----------------------------------------------------------------------------------------
转载的时候请注明出处




支持 iPv6：
1、Extra packages  --->  ipv6helper  （选定这个后下面几项自动选择了）
Network  --->  odhcp6c
Network  --->  odhcpd-ipv6only
LuCI  --->  Protocols  --->  luci-proto-ipv6
LuCI  --->  Protocols  --->  luci-proto-ppp

2、打开适用于VMware的VM Tools
Utilities  --->  open-vm-tools  #打开适用于VMware的VM Tools
Utilities  --->  open-vm-tools-fuse  #打开适用于VMware的VM Tools

3、第二次编译：
cd lede                                                                               # 进入LEDE目录
git pull                                                                                # 同步更新L大源码
./scripts/feeds update -a && ./scripts/feeds install -a               # 更新Feeds
rm -rf ./tmp && rm -rf .config                                               # 清除编译配置和缓存
make menuconfig                                                                # 进入编译配置菜单
make -jn V=99                                                                    # 开始编译 n=线程数+1，例如4线程的I5填-j5

4、编译丰富插件时，建议修改下面两项默认大小，留足插件空间。（x86/64）！！！
Target Images ---> (16) Kernel partition size (in MB)                        #默认是 (16) 建议修改 (256)
Target Images ---> (160) Root filesystem partition size (in MB)        #默认是 (160) 建议修改 (512)


## License

[MIT](https://github.com/P3TERX/Actions-OpenWrt/blob/main/LICENSE) © [**P3TERX**](https://p3terx.com)
