# 🚀 GitHub加速神器，妈妈再也不怕我登不上了

## 📖 引言

不科学上网的话，GitHub经常登不上，经常clone项目和push项目报下面这种错，就很烦。无意中发现了这个利器，解决了我很久以来的痛点。现在推给大家用用。
```
fatal: unable to access ‘[https://github.com/user/repo.git/](https://github.com/user/repo.git/)‘: Failed to connect to github.com port 443: Connection refused
```

## 🔍 工具介绍

FastGithub是一款专为解决GitHub访问问题的开源工具，主要功能包括：

- 🌐 ‌**纯净IP解析**‌：自动选择最快的GitHub服务器IP
- ⚡ ‌**TLS优化**‌：自定义域名TLS连接配置
- 📦 ‌**CDN替换**‌：解决国外JS/CSS资源加载失败问题
- 🔒 ‌**本地代理**‌：通过38457端口提供加速服务（非VPN）

> 📢 注意：该工具‌**不具备翻墙功能**‌，仅优化GitHub本身的访问体验

## 💻 安装与使用指南

官网地址：[github地址](https://github.com/creazyboyone/FastGithub?tab=readme-ov-file)

### 🪟Windows系统

- [y] **桌面版**:双击运行 FastGithub.UI.exe  
- [y] **服务版**: fastgithub.exe start(安装并启动服务)/fastgithub.exe stop(卸载服务)

### 🐧 Linux系统

- [y] **终端模式**: 
```bash
sudo ./fastgithub 
```
- [y] **服务模式**: 
```bash
sudo ./fastgithub start
```
- [y] **两种模式都需设置代理**: 
```bash
git config --global http.proxy http://127.0.0.1:38457 
git config --global https.proxy http://127.0.0.1:38457
```

### 🍎 macOS系统

1. 双击运行fastgithub
2. 安装并信任 `cacert/fastgithub.cer`
3. 设置系统代理为 `127.0.0.1:38457`

### 🐳 Docker部署

1. 准备好docker 18.09, docker-compose.
2. 在源码目录下，有一个docker-compose.yaml 文件，专用于在实际项目中，临时使用github.com源码，而做的demo配置。
3. 根据自己的需要更新docker-compose.yaml中的sample和build镜像即可完成拉github.com源码加速，并基于源码做后续的操作。

## 🔧 常见问题处理

- ‌**Git证书错误**‌：  
    git操作提示`SSL certificate problem`  
	需要关闭git的证书验证：`git config --global http.sslverify false`
    
- ‌**Firefox安全警告**‌：  
    firefox提示`连接有潜在的安全问题`  
	设置->隐私与安全->证书->查看证书->证书颁发机构，导入cacert/fastgithub.cer，勾选“信任由此证书颁发机构来标识网站”
  

## ⚠️ 重要安全提示

1. CA证书保存在`cacert`文件夹，请勿泄露私钥
2. 该工具完全遵守《国际联网暂行规定》，仅优化现有网络通道