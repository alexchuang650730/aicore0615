# 🌐 PowerAutomation 完整Web访问链接指南

## 🎯 **主要Web服务链接**

### **🏠 主界面 - AI智能开发平台**
- **主页面**: http://98.81.255.168:5001
- **API状态**: http://98.81.255.168:5001/api/status
- **聊天API**: http://98.81.255.168:5001/api/chat

### **🔧 三个专业MCP服务Web界面**
- **🧪 Test Manager MCP**: http://98.81.255.168:8097
- **🚀 Release Manager MCP**: http://98.81.255.168:8096
- **📊 Operations Workflow MCP**: http://98.81.255.168:8090

## 🎮 **核心功能链接**

### **🤖 AI代码生成**
- **主界面**: http://98.81.255.168:5001
- **功能**: 输入项目需求，AI生成完整代码
- **支持**: 游戏、网站、应用、系统等各种项目

### **📦 三个智能按钮**
访问主界面后可使用：
1. **下载完整代码** - 获取所有项目文件
2. **🎮 在线预览** - 实时查看项目效果
3. **📚 查看文档** - 技术文档和说明

## 🔌 **API直接访问**

### **生成项目代码**
```bash
curl -X POST -H "Content-Type: application/json" \
  -d '{"message":"我要开发贪吃蛇游戏"}' \
  http://98.81.255.168:5001/api/chat
```

### **检查系统状态**
```bash
curl http://98.81.255.168:5001/api/status
```

### **检查MCP服务**
```bash
curl http://98.81.255.168:8097/api/status  # Test Manager
curl http://98.81.255.168:8096/api/status  # Release Manager
curl http://98.81.255.168:8090/api/status  # Operations
```

## 🛠️ **如果Web界面无法访问**

### **方案一：SSH隧道** (推荐)
```bash
# 创建本地隧道
ssh -L 8080:localhost:5001 -i alexchuang.pem ec2-user@98.81.255.168

# 然后访问
http://localhost:8080
```

### **方案二：多端口隧道**
```bash
# 创建所有服务的隧道
ssh -L 8080:localhost:5001 \
    -L 8090:localhost:8090 \
    -L 8096:localhost:8096 \
    -L 8097:localhost:8097 \
    -i alexchuang.pem ec2-user@98.81.255.168

# 访问链接
http://localhost:8080  # 主界面
http://localhost:8090  # Operations MCP
http://localhost:8096  # Release Manager MCP
http://localhost:8097  # Test Manager MCP
```

### **方案三：使用API工具**
- **Postman**: 导入API端点
- **Insomnia**: 创建API集合
- **Thunder Client**: VS Code插件

## 🚀 **快速开始**

### **1. 访问主界面**
```
http://98.81.255.168:5001
```

### **2. 输入项目需求**
例如：
- "我要开发一个计算器"
- "创建一个图书管理系统"
- "制作一个贪吃蛇游戏"

### **3. 使用三个按钮**
- 📦 下载完整代码
- 🎮 在线预览
- 📚 查看文档

## 📊 **服务状态**

| 服务 | 链接 | 端口 | 状态 | 功能 |
|------|------|------|------|------|
| 主界面 | http://98.81.255.168:5001 | 5001 | ✅ 运行中 | AI代码生成 |
| Test Manager | http://98.81.255.168:8097 | 8097 | ✅ 运行中 | 智能测试 |
| Release Manager | http://98.81.255.168:8096 | 8096 | ✅ 运行中 | 智能部署 |
| Operations | http://98.81.255.168:8090 | 8090 | ✅ 运行中 | 运维管理 |

## 🎯 **7个专业工作流**

PowerAutomation包含完整的软件开发生命周期：

1. **📋 需求分析** - Requirements Analysis MCP
2. **🏗️ 架构设计** - Architecture Design MCP
3. **💻 编码实现** - Coding Workflow MCP
4. **👨‍💻 开发流程** - Developer Flow MCP
5. **🧪 测试管理** - Test Manager MCP
6. **🚀 发布管理** - Release Manager MCP
7. **📊 运维管理** - Operations Workflow MCP

## 🎉 **立即开始**

**主要链接**: http://98.81.255.168:5001

现在就可以开始使用您的PowerAutomation AI开发平台！🚀

---

**注意**: 如果遇到504超时问题，请使用SSH隧道方案或API直接调用。所有核心功能完全正常！

