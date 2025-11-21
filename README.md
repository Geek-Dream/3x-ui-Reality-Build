# 3x-ui-Reality-build
搭建并且确保支持 Reality 协议

执行命令
```bash
# 卸载x-ui
x-ui uninstall
# 停止x-ui
systemctl stop x-ui
systemctl disable x-ui

# 彻底清理x-ui
rm -f /etc/systemd/system/x-ui.service
rm -rf /usr/local/x-ui
rm -rf /etc/x-ui

# 3x-ui 官方标准版
bash <(curl -Ls https://raw.githubusercontent.com/mhsanaei/3x-ui/master/install.sh)

# 3x-ui 汉化包 centos8才可以
bash <(curl -Ls https://raw.githubusercontent.com/gm-cx/3x-ui-cn/master/install.sh)

```

## 执行命令好之后选择n，运行结果如下

Would you like to customize the Panel Port settings? (If not, a random port will be applied) [y/n]: n

Generated random port: xxxxx

Port set successfully: xxxxx

Username and password updated successfully

Base URI path set successfully

This is a fresh installation, generating random login info for security concerns:

###############################################

Username: xxxxx

Password: xxxxx

Port: xxxxx

WebBasePath: xxxxx

Access URL: http://111.11.111.111:1111/xxxxxxxxx

###############################################

Start migrating database...

Migration done!

Created symlink /etc/systemd/system/multi-user.target.wants/x-ui.service → /etc/systemd/system/x-ui.service.

x-ui v2.8.5 installation finished, it is running now...


┌───────────────────────────────────────────────────────┐
│  x-ui control menu usages (subcommands):              │
│                                                       │
│  x-ui              - Admin Management Script          │
│  x-ui start        - Start                            │
│  x-ui stop         - Stop                             │
│  x-ui restart      - Restart                          │
│  x-ui status       - Current Status                   │
│  x-ui settings     - Current Settings                 │
│  x-ui enable       - Enable Autostart on OS Startup   │
│  x-ui disable      - Disable Autostart on OS Startup  │
│  x-ui log          - Check logs                       │
│  x-ui banlog       - Check Fail2ban ban logs          │
│  x-ui update       - Update                           │
│  x-ui legacy       - Legacy version                   │
│  x-ui install      - Install                          │
│  x-ui uninstall    - Uninstall                        │
└───────────────────────────────────────────────────────┘

## 因为x-ui 3的特殊情况，你只能通过本机ssh连接访问
1. 首先windos电脑和mac电脑执行连接方法不一样如下：
2. 首先windos打开cmd并且管理员输入：ssh -L 15208:127.0.0.1:xxxx root@xxxx.xxxx.xxx.xx
3. 然后输入VPS的密码登录
4. 打开网页并且输入你的地址就是127.0.0.1:xxxxx

1. 如果使用mac的话，直接使用终端
2. 输入链接：ssh -L 15208:127.0.0.1:xxxx root@xxxx.xxxx.xxx.xx
3. 然后如果第一次使用ssh那么使用yes
4. 最后输入VPS的登录密码
5. 打开网页并且输入你的地址就是127.0.0.1:xxxxx




## 打开页面之后进行配置
1. 选择左侧入站列表 -> 添加入站
2. 输入vless协议
3. 监听不用输入，默认对外开放
4. 端口可以随机生成无所谓
5. 总流量自己设置
6. 设备限制无所谓，到期时间自己看，可以不设置
7. 打开客户/用户，启用，输入电子邮件，或者自动生成电子邮件
8. 然后随机ID，限速自己设置，评论自己设置无所谓不重要flow默认选择'xtls-rprx-vision'
9. 总流量根据自己用户进行分配
10. 选择tcp协议
11. Proxy Protocol关闭，HTTP伪装关闭，Sockopt关闭，External Proxy关闭
12. 选择Reality协议，打开Show，Xver默认0，uTLS选择chrome
13. Target选择伪装的节点，确保你的地址大陆可以访问的外网节点，默认可以使用443，如下：abc.abc.abc:443
14. 然后SNI和上面一样，但是不用输入端口如下:abc.abc.abc
15. Max Time 默认0，Min Client Ver和Max Client Ver均为空
16. Short IDs 清空
17. SpiderX 选择 /
18. 点击获取随机证书，生成公钥和密钥。
19. 然后点保存，之后点击感叹号获取vless链接地址
20. 开心使用吧




