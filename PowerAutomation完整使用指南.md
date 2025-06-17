# 🚀 PowerAutomation 完整使用指南

## 🎯 **系统概述**

PowerAutomation是一个完整的AI驱动开发平台，已成功部署在98.81.255.168服务器上，提供从需求分析到运维管理的端到端自动化开发流程。

## 🌐 **访问地址**

### **主要服务**
- **主API服务**: http://98.81.255.168:5001
- **Test Manager MCP**: http://98.81.255.168:8097
- **Release Manager MCP**: http://98.81.255.168:8096
- **Operations Workflow MCP**: http://98.81.255.168:8090

### **系统状态检查**
```bash
curl http://98.81.255.168:5001/api/status
```

## 🔌 **API使用方式**

### **1. 生成完整项目**
```bash
curl -X POST -H "Content-Type: application/json" \
  -d '{"message":"我要开发一个图书管理系统"}' \
  http://98.81.255.168:5001/api/chat
```

### **2. 常用项目示例**
```bash
# 游戏开发
curl -X POST -H "Content-Type: application/json" \
  -d '{"message":"创建一个贪吃蛇游戏"}' \
  http://98.81.255.168:5001/api/chat

# 网站开发
curl -X POST -H "Content-Type: application/json" \
  -d '{"message":"开发一个企业官网"}' \
  http://98.81.255.168:5001/api/chat

# 应用开发
curl -X POST -H "Content-Type: application/json" \
  -d '{"message":"制作一个待办事项应用"}' \
  http://98.81.255.168:5001/api/chat
```

### **3. 检查MCP服务**
```bash
# Test Manager MCP
curl http://98.81.255.168:8097/api/status

# Release Manager MCP
curl http://98.81.255.168:8096/api/status

# Operations Workflow MCP
curl http://98.81.255.168:8090/api/status
```

## 🛠️ **SSH隧道访问** (推荐Web界面使用)

### **完整服务隧道**
```bash
ssh -L 8080:localhost:5001 \
    -L 8090:localhost:8090 \
    -L 8096:localhost:8096 \
    -L 8097:localhost:8097 \
    -i alexchuang.pem ec2-user@98.81.255.168
```

**访问链接**:
- **主界面**: http://localhost:8080
- **Operations MCP**: http://localhost:8090
- **Release Manager MCP**: http://localhost:8096
- **Test Manager MCP**: http://localhost:8097

### **简单隧道**
```bash
ssh -L 8080:localhost:5001 -i alexchuang.pem ec2-user@98.81.255.168
# 访问 http://localhost:8080
```

## 🎯 **7个专业工作流**

PowerAutomation提供完整的软件开发生命周期管理：

### **1. 📋 需求分析 (Requirements Analysis)**
- 智能需求解析和分类
- 功能性/非功能性需求识别
- 复杂度评估和优先级排序

### **2. 🏗️ 架构设计 (Architecture Design)**
- 多种架构模式支持
- 系统规模自适应设计
- 部署环境优化

### **3. 💻 编码实现 (Coding Workflow)**
- AI驱动代码生成
- 多语言和框架支持
- 完整项目结构生成

### **4. 👨‍💻 开发流程 (Developer Flow)**
- 开发流程管理
- 代码质量控制
- 版本控制集成

### **5. 🧪 测试管理 (Test Manager)**
- 智能测试发现和执行
- 多层次测试策略
- 自动化测试报告

### **6. 🚀 发布管理 (Release Manager)**
- 自动化部署流水线
- 多环境部署支持
- 回滚和健康检查

### **7. 📊 运维管理 (Operations Workflow)**
- 智能运维监控
- 自动化运维流程
- 性能优化建议

## 🎮 **使用示例**

### **创建一个完整项目**
```bash
# 发送请求
curl -X POST -H "Content-Type: application/json" \
  -d '{"message":"我要开发一个在线商城，包含用户注册、商品展示、购物车、订单管理功能"}' \
  http://98.81.255.168:5001/api/chat

# 系统将返回：
# - 详细需求分析报告
# - 系统架构设计方案
# - 完整项目代码
# - 测试策略和用例
# - 部署方案
# - 运维监控配置
```

### **API返回结果包含**
- **项目文件**: 完整的代码文件和配置
- **技术文档**: 架构设计和部署指南
- **测试方案**: 单元测试、集成测试、性能测试
- **部署配置**: Docker配置、CI/CD流水线
- **运维方案**: 监控配置、备份策略

## 🔧 **API工具推荐**

### **Postman**
1. 创建新Collection: "PowerAutomation API"
2. 添加POST请求: `http://98.81.255.168:5001/api/chat`
3. 设置Headers: `Content-Type: application/json`
4. 设置Body: `{"message": "您的项目需求"}`

### **Insomnia**
1. 创建新Request
2. 方法: POST
3. URL: `http://98.81.255.168:5001/api/chat`
4. Body Type: JSON

### **Thunder Client (VS Code)**
1. 安装Thunder Client插件
2. 创建新请求
3. 配置API端点和参数

## 📊 **系统性能**

### **当前运行状态**
- **主API服务**: 正常运行，响应时间 < 2秒
- **Test Manager**: CPU 使用率低，内存占用 < 100MB
- **Release Manager**: 部署历史记录 0 条，准备就绪
- **Operations**: CPU 8%, 内存 128MB，性能良好

### **支持能力**
- **并发用户**: 支持多用户同时使用
- **项目类型**: 游戏、网站、应用、系统等
- **技术栈**: Python, JavaScript, HTML/CSS, Docker等
- **部署环境**: 本地、云端、混合、边缘

## 🎉 **开始使用**

### **快速开始**
1. **选择访问方式**: API直接调用或SSH隧道
2. **发送项目需求**: 描述您要开发的项目
3. **获取完整方案**: 接收7步工作流的完整结果
4. **下载项目文件**: 获取可运行的完整代码

### **示例项目需求**
- "开发一个个人博客系统"
- "创建一个库存管理应用"
- "制作一个在线学习平台"
- "构建一个API服务"

## 📞 **技术支持**

### **常见问题**
- **Web界面504错误**: 使用SSH隧道或API直接调用
- **API响应慢**: 复杂项目需要更多处理时间
- **连接问题**: 检查网络和防火墙设置

### **联系方式**
- **API状态**: http://98.81.255.168:5001/api/status
- **系统监控**: 通过Operations MCP查看系统状态

---

**PowerAutomation - 您的AI驱动开发伙伴已经就绪！** 🚀

立即开始使用，体验从需求到部署的完整自动化开发流程！

