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
