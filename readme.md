# v2ray-subscriber

这是一个适用于 v2ray 的服务器代理订阅器，可以帮助你很方便地从订阅链接中获取、测试和切换代理服务器。仅在 Arch Linux 下有过测试。

## 使用方式

本脚本采用 Python3 编写，直接调用 v2ray 命令及直接更改 v2ray 的配置文件。所以，您需要安装 python3 跟 v2ray 才能使用。

使用本脚本很简单，以 root 用户身份执行即可。因为本脚本会写入 v2ray 的 config.json 和重启 v2ray 的服务，所以需要您提供 root 权限。 `sudo ./v2sub`

另：本脚本使用过程式编程模式书写，以及 config.json 的内容都是硬编码在脚本内的。执行本脚本会覆盖您在 /etc/v2ray 中的 config.json 文件。如果您想修改默认端口等配置，您可以直接编辑本脚本文件~~或者去自己写~~。

当您使用过后，您可以将本脚本的软连接添加至 `/usr/bin` 或者其他的什么地方，这样您在想换代理服务器时，只需要在终端敲 `v2sub` 就好了。

## 在 Arch Linux 下安装 v2ray
```
sudo pacman -S v2ray
systemctl enable v2ray.service
```