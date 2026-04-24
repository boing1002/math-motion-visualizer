# 行程问题可视化工具 v3.0 | Math Motion Visualizer

> 帮助数学老师通过动态动画演示行程问题，让学生直观理解抽象的运动过程。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://www.w3.org/html/)
[![Canvas](https://img.shields.io/badge/Canvas-000000?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![Version](https://img.shields.io/badge/Version-3.0-brown.svg)](https://github.com/boing1002/math-motion-visualizer)

## ✨ v3.0 核心特性

### 🎯 三大模块全覆盖

- **模块1: 直线往返相遇问题** - 折返轨迹自动下移,清晰显示累积路程
- **模块2: 直线单次追及问题** - 平行跑道展示,初始差距可视化
- **模块3: 环形多次相遇/追及问题** - 双屏联动,环形+直线展开图

### 🚀 教学创新

- ✅ **轨迹下移** - 折返跑时轨迹自动下移,形成"楼梯"效果
- ✅ **双屏联动** - 环形视图+条形图,化曲为直
- ✅ **自动暂停** - 相遇/追上时自动暂停,弹出验证公式
- ✅ **实时数据** - 路程、时间、圈数实时更新
- ✅ **参数可配** - 速度、距离、初始差距自由设置

### 🎨 Notion风格设计

- 🤎 温暖的米白色调
- 📝 优雅的衬线字体
- 🎯 清晰的信息层级
- 📱 响应式布局

## 🚀 快速开始

### 方式1：直接打开（推荐）

```bash
# 下载整个项目文件夹
# 双击打开 index.html
```

### 方式2：本地服务器

```bash
# 使用Python启动简单服务器
python3 -m http.server 8000

# 访问 http://localhost:8000
```

### 方式3：Cloudflare Pages 部署

```bash
# 1. 推送到 GitHub
git push origin main

# 2. 在 Cloudflare Pages 连接仓库
# 3. 自动部署完成
```

## 📸 功能预览

### 模块1: 直线往返相遇

```
特点: 折返轨迹下移
- 两端出发 / 同端出发
- 每次折返轨迹下移60px
- 自动显示相遇点垂直虚线
- 验证公式: (2n-1)S 或 2nS
```

### 模块2: 直线单次追及

```
特点: 平行跑道展示
- 甲在上跑道(快),乙在下跑道(慢)
- 黄色箭头标记初始差距
- 绿色箭头标记共同路程
- 验证公式: 甲路程 = 初始差距 + 乙路程
```

### 模块3: 环形多次相遇/追及

```
特点: 双屏联动
- 左侧: 环形视图(圆形跑道)
- 右侧: 直线展开图(累积圈数条形图)
- 支持相向而行(相遇)和同向而行(追及)
- 验证公式: n次相遇=n圈, n次追及=n圈差
```

## 🎓 使用场景示例

### 场景1: 直线往返相遇

```
题目: 甲乙在100米直线上往返跑
      甲速度5m/s,乙速度3m/s
      两端出发,第3次相遇时共跑多少米?

操作:
1. 打开 index.html
2. 选择"直线往返相遇"标签
3. 配置: 距离100m,甲5m/s,乙3m/s,两端出发
4. 点击"开始演示"
5. 观察3次相遇,自动显示验证公式

答案: 5S = 500米 ✅
```

### 场景2: 直线单次追及

```
题目: 甲乙在100米跑道上
      甲速度8m/s,乙速度6m/s
      乙领先20米,甲多久追上?

操作:
1. 选择"直线单次追及"标签
2. 配置: 甲8m/s,乙6m/s,初始差距20m
3. 点击"开始演示"
4. 观察追上过程,黄色箭头显示初始差距

答案: 10秒 ✅
```

### 场景3: 环形多次追及

```
题目: 甲乙在400米环形跑道
      甲速度5m/s,乙速度3m/s
      同点同向出发,第2次追上时总路程?

操作:
1. 选择"环形多次相遇/追及"标签
2. 配置: 相同方向,同点出发
3. 点击"开始演示"
4. 左侧看环形运动,右侧看累积圈数

答案: 甲乙共跑 1600米 = 4圈 ✅
```

## 🛠️ 技术栈

- **HTML5** - 页面结构
- **CSS3** - Notion风格样式
- **Vanilla JavaScript** - 核心逻辑(零依赖)
- **Canvas API** - 动画绘制
- **LocalStorage** - 本地存储(模块1)

## 📦 项目结构

```
.
├── index.html                      # 主入口(Tab切换)
├── 模块1-直线往返相遇.html          # 模块1独立文件
├── 模块2-直线单次追及.html          # 模块2独立文件
├── 模块3-环形多次相遇追及.html      # 模块3独立文件
├── README.md                       # 项目说明
├── FINAL_PLAN_V3.md               # v3.0最终方案
├── MODULE1_DESIGN.md              # 模块1详细设计
├── AI_SUGGESTION_ANALYSIS.md      # AI建议分析
├── TEACHING_DIFFICULTIES.md       # 教学难点分析
└── .gitignore                      # Git忽略文件
```

## 🎨 设计系统

本项目采用 **Notion风格** 设计系统：

```css
/* 颜色系统 */
--bg-primary: #F7F6F3;      /* 温暖米白 */
--bg-secondary: #FFFFFF;    /* 纯白卡片 */
--accent-brown: #C28B5D;    /* 棕色强调 */
--accent-red: #E03E3E;      /* 甲颜色 */
--accent-blue: #5E8AD2;     /* 乙颜色 */
--accent-gold: #D4952A;     /* 初始差距 */

/* 字体系统 */
--font-serif: 'Georgia';    /* 标题 */
--font-sans: 系统字体;       /* 正文 */
```

## 📖 文档

- [FINAL_PLAN_V3.md](FINAL_PLAN_V3.md) - v3.0完整实现方案
- [MODULE1_DESIGN.md](MODULE1_DESIGN.md) - 模块1详细设计
- [AI_SUGGESTION_ANALYSIS.md](AI_SUGGESTION_ANALYSIS.md) - AI建议分析
- [TEACHING_DIFFICULTIES.md](TEACHING_DIFFICULTIES.md) - 教学难点分析

## 🚀 部署指南

### Cloudflare Pages 部署

1. **推送代码到 GitHub**
   ```bash
   git add .
   git commit -m "Release v3.0"
   git push origin main
   ```

2. **连接 Cloudflare Pages**
   - 访问 https://pages.cloudflare.com/
   - 点击 "Create a project"
   - 选择 GitHub 仓库
   - 构建设置留空(纯静态HTML)

3. **访问网站**
   - 获得一个 `*.pages.dev` 域名
   - 自动HTTPS + 全球CDN

### Vercel 部署

```bash
# 安装 Vercel CLI
npm i -g vercel

# 部署
vercel --prod
```

## 🤝 贡献

欢迎贡献代码、报告问题或提出新功能建议！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📝 开发路线图

### v3.1 计划
- [ ] 添加预设题目系统(10+经典题型)
- [ ] 支持导出动画为GIF
- [ ] 添加慢动作回放功能

### v4.0 愿景
- [ ] 多物体追及(3-4个物体)
- [ ] 非同点出发的环形问题
- [ ] 复杂场景:走走停停+变速

## 📄 许可证

[MIT License](LICENSE)

## 🙏 致谢

- 设计灵感来自 [Notion](https://notion.so)
- 参考了 [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) 的设计系统
- 感谢 Claude Code 提供技术实现

## 📮 联系方式

- GitHub: [boing1002/math-motion-visualizer](https://github.com/boing1002/math-motion-visualizer)
- 问题反馈: [GitHub Issues](https://github.com/boing1002/math-motion-visualizer/issues)

---

**Made with ❤️ for math teachers and students**

**v3.0 - 完整三模块版本** | 2026-04
