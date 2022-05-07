# [教程] 如何录制 B 站直播

# 工具1：[blrec](https://github.com/acgnhiki/blrec) （有图形操作界面，是个网页）
本地运行例子（如果你本地装了 Docker，直接运行这条命令）：
```
sudo docker run \
    -v /etc/blrec:/cfg -v /var/log/blrec:/log -v ~/blrec:/rec \
    -dp 2233:2233 acgnhiki/blrec \
    -c /cfg/another_settings.toml
```
随后访问 `localhost:2233` 即可。

# 工具2：[bililive-go](https://github.com/hr3lxphr6j/bililive-go) (纯命令行）
优点：单文件，下载即用，纯命令行使用。

如何安装：
在 Release 页面安装适合你的版本，   
比如我 macOS 用的是 0.63 版本的 `bililive-darwin-amd64.tar.gz`

本地运行例子：
```
./bililive-darwin-amd64 -i https://live.bilibili.com/23070000
```

# 结论
如果你只是轻度使用，就录这么一两次，那么以上哪个工具都可以，随便用。   
如果你是重度使用，希望 24x7 一旦主播开播了就录制，  
那么建议你自己找个云服务器 腾讯云/阿里云，或者什么别的服务器（我没试过 Digital Ocean 或者 Google Cloud 等服务商）   
自己搭一个 blrec。  
