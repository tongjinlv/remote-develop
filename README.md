# Remote Dev Assistant - VS Code 插件

🚀 **自动同步本地文件到远程服务器 + 一键执行远程命令**，提升远程开发效率，交叉开发利器！

## 功能亮点
- 🔄 **实时文件同步** - 本地文件修改后自动上传到远程服务器
- ⚡ **一键执行远程命令** - 按 `F5` 快速运行服务器上的脚本/程序
- 📜 **终端输出集成** - 直接在 VS Code 输出面板查看远程执行结果
- 🔒 **SSH 密钥支持** - 安全连接，无需频繁输入密码

---

## 快速开始
### 1. 安装插件
在 VS Code 扩展商店搜索 **"Remote Develop"** 并安装。

### 2. 配置 SSH 连接
在项目 `.vscode/config.json` 中添加你的服务器信息：
```json
{
  "ssh": {
    "host": "your-server-ip",          //远程服务器域名或者ip 
    "port": 22,                        //远程服务器登录端口
    "username": "your-username",       //远程服务器登录名
    "privateKeyPath": "~/.ssh/id_rsa"  // 远程服务器私钥
  },
  "remoteBasePath": "/home/your-username/project",  // 远程服务器路径
  "runCommand": "make"                   // 按 F5 执行的命令
}
