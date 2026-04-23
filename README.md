# 行程问题可视化工具 | Math Motion Visualizer

> 帮助数学老师通过动态动画演示行程问题，让学生直观理解抽象的运动过程。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://www.w3.org/html/)
[![Canvas](https://img.shields.io/badge/Canvas-000000?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)

## ✨ 特性

- 🎯 **4种场景**：环形追击、直线相遇、直线往返、走走停停
- 🚗 **2-4个物体**：灵活配置运动物体数量和参数
- 🎨 **Notion风格UI**：温暖、专业的设计语言
- 💾 **题库系统**：预设题目 + 本地保存自定义配置
- ⚡ **零依赖**：纯HTML文件，双击即用
- 📱 **响应式**：支持桌面和移动设备

## 🚀 快速开始

### 方式1：直接打开（推荐）

```bash
# 下载文件后双击打开
行程问题可视化.html
```

### 方式2：本地服务器

```bash
# 使用Python启动简单服务器
python3 -m http.server 8000

# 访问 http://localhost:8000
```

### 方式3：在线预览

🔗 **[点击这里在线体验](https://your-cloudflare-pages-url.com)** （部署后更新链接）

## 📸 功能截图

### 环形跑道追击
![环形追击](docs/images/circular.png)

### 直线相遇问题
![直线相遇](docs/images/linear.png)

### 走走停停模式
![走走停停](docs/images/stop-go.png)

## 🎓 使用场景

### 场景1：环形跑道追击
```
题目：甲乙两人在400米环形跑道上跑步
      甲的速度是6 km/h，乙的速度是8 km/h
      如果两人同时从同一点出发同向跑步
      乙多久能追上甲？

操作：选择"环形跑道追击" → 点击播放 → 观察追上过程

答案：12分钟
```

### 场景2：直线相遇问题
```
题目：A、B两地相距225公里
      甲、乙两车分别从A、B两地同时出发，相向而行
      甲车速度60 km/h，乙车速度72 km/h
      问两车多久后相遇？

操作：选择"直线相遇问题" → 点击播放 → 观察相遇过程

答案：约102分钟
```

### 场景3：走走停停（复杂）
```
题目：甲车从A出发，速度60 km/h
      每行驶45分钟停5分钟校准信号
      乙车从B出发，速度72 km/h
      每行驶25分钟停5分钟校准信号
      两车同时出发相向而行，问多久后相遇？

操作：
1. 选择"走走停停模式"
2. 配置甲车：跑45分钟，停5分钟
3. 配置乙车：跑25分钟，停5分钟
4. 点击播放 → 观察停顿状态变化

答案：116分钟
```

## 🛠️ 技术栈

- **HTML5** - 页面结构
- **CSS3** - Notion风格样式
- **Vanilla JavaScript** - 核心逻辑
- **Canvas API** - 动画绘制
- **LocalStorage** - 本地存储

## 📖 文档

- [产品需求文档（PRD）](PRD.md) - 完整的功能规格说明
- [使用指南](docs/GUIDE.md) - 详细使用教程
- [API文档](docs/API.md) - 开发者API参考

## 🎨 设计系统

本项目采用 **Notion风格** 设计系统：

```css
/* 颜色系统 */
--bg-primary: #F7F6F3;      /* 温暖米白 */
--bg-secondary: #FFFFFF;    /* 纯白卡片 */
--accent-brown: #C28B5D;    /* 棕色强调 */

/* 字体系统 */
--font-serif: 'Georgia';    /* 标题 */
--font-sans: 系统字体;       /* 正文 */
```

详见 [PRD.md - UI设计规范](PRD.md#4-ui设计规范notion风格)

## 📦 项目结构

```
.
├── 行程问题可视化.html    # 主文件（单文件应用）
├── PRD.md                  # 产品需求文档
├── README.md               # 项目说明
├── .gitignore              # Git忽略文件
└── docs/                   # 文档目录
```

## 🤝 贡献

欢迎贡献代码、报告问题或提出新功能建议！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📝 开发计划

- [x] MVP功能实现
- [ ] 添加更多预设题目（目标20+）
- [ ] 多视角切换功能
- [ ] 导出GIF/视频
- [ ] 答题验证模式
- [ ] 云端题库系统

## 📄 许可证

[MIT License](LICENSE)

## 🙏 致谢

- 设计灵感来自 [Notion](https://notion.so)
- 参考了 [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) 的设计系统

## 📮 联系方式

- 问题反馈：[GitHub Issues](https://github.com/your-username/math-motion/issues)
- 邮箱：your-email@example.com

---

**Made with ❤️ for math teachers and students**
