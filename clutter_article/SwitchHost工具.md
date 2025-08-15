## **📜 引言 **

😫 你是否经常遇到这样的烦恼？  
开发时需要切换测试环境，访问不同域名却要手动修改hosts文件；  
每次改完还要刷新DNS缓存，操作繁琐又容易出错...  
今天给大家安利一个神器——‌**SwitchHosts**‌！  
✨ 它能让你的主机管理变得像切换电视频道一样简单！

---

## **🔍 SwitchHosts是什么？**

📌 SwitchHosts是一个‌**跨平台的主机管理工具**‌，支持Windows/macOS/Linux系统。  
它的核心功能：  
✅ 可视化编辑hosts文件  
✅ 支持多组hosts配置快速切换  
✅ 自动刷新DNS缓存（无需重启）  
✅ 支持导入导出配置  
✅ 开源免费（GitHub 30k+ stars）

💡 特别适合：  
• 前后端开发者  
• 测试工程师  
• 需要频繁切换环境的运维人员

---

## **🎯 安装使用指南 **

### 1. 安装方式

#### Windows系统

1️⃣ 官网下载：https://github.com/oldj/SwitchHosts/releases  
2️⃣ 解压后直接运行`SwitchHosts.exe`

#### macOS系统

🎯 推荐使用Homebrew安装：

bashCopy Code

`brew install --cask switchhosts`

### 2. 基础操作

1. ‌**添加hosts组**‌  
    👉 点击左侧"+"号 → 输入组名 → 粘贴hosts内容
    
2. ‌**切换配置**‌  
    🔄 双击组名即可立即生效
    
3. ‌**编辑规则**‌  
    ✏️ 支持语法高亮，格式示例：
    
    textCopy Code
    
    `127.0.0.1   test.example.com`
    

---

## **👨‍💻实战用例场景**

### 场景1：本地开发环境切换

🖥️ 前端开发时经常需要：  
• 测试环境 → 生产环境  
• 本地Mock API → 真实API  
用SwitchHosts可保存多套配置，一键切换！

### 场景2：临时屏蔽广告

🚫 想屏蔽某个烦人的广告？  
添加规则：

textCopy Code

`0.0.0.0 ad.example.com`

再也不用担心被广告弹窗打扰~

### 场景3：多项目管理

👨‍💻 同时维护多个项目时，每个项目对应独立的hosts配置：  
• 项目A → 配置A  
• 项目B → 配置B  
避免配置混乱，提升工作效率！