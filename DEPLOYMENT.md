# Cloudflare Pages 部署指南

## 📦 仓库信息

- **GitHub仓库**: https://github.com/boing1002/math-motion-visualizer
- **项目类型**: 静态HTML网站（单文件应用）
- **主文件**: `行程问题可视化.html`

---

## 🚀 方式1：通过Cloudflare Dashboard部署（推荐）

### 步骤1：登录Cloudflare
1. 访问 [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. 登录你的Cloudflare账号

### 步骤2：创建Pages项目
1. 在左侧菜单选择 **Workers & Pages** → **Create application**
2. 选择 **Pages** 标签
3. 点击 **Connect to Git**

### 步骤3：连接GitHub仓库
1. 点击 **Connect GitHub**
2. 授权Cloudflare访问你的GitHub账号
3. 选择仓库：**boing1002/math-motion-visualizer**

### 步骤4：配置构建设置
由于是纯静态HTML文件，**不需要构建命令**：

```
项目名称: math-motion-visualizer (或自定义)
生产分支: main
构建命令: (留空)
构建输出目录: / (根目录)
```

### 步骤5：环境变量（可选）
无需环境变量，跳过此步骤。

### 步骤6：部署
1. 点击 **Save and Deploy**
2. 等待部署完成（约30秒）
3. 获得部署URL：`https://math-motion-visualizer.pages.dev`

---

## 🚀 方式2：通过Wrangler CLI部署

### 前置条件
安装Node.js和Wrangler CLI：

```bash
npm install -g wrangler
```

### 步骤1：登录Cloudflare
```bash
wrangler login
```

### 步骤2：创建部署配置
在项目根目录创建 `wrangler.toml`：

```toml
name = "math-motion-visualizer"
type = "javascript"
account_id = "your-account-id"  # 可选
workers_dev = true

[site]
bucket = "/"
```

### 步骤3：部署
```bash
wrangler pages deploy . --project-name=math-motion-visualizer
```

---

## 🚀 方式3：直接上传文件（最简单）

### 步骤1：准备文件
确保 `行程问题可视化.html` 在项目根目录。

### 步骤2：上传到Cloudflare Pages
1. 访问 [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. 选择 **Workers & Pages** → **Create application**
3. 选择 **Upload assets**
4. 拖拽 `行程问题可视化.html` 到上传区域
5. 点击 **Deploy site**

---

## 🎯 自定义域名（可选）

### 添加自定义域名
1. 在Cloudflare Pages项目中
2. 选择 **Custom domains**
3. 点击 **Set up a custom domain**
4. 输入你的域名（如：`math.yourdomain.com`）
5. 按照提示配置DNS记录

---

## 🔄 自动部署

配置完成后，每次推送到 `main` 分支会自动触发部署：

```bash
git add .
git commit -m "更新内容"
git push origin main
```

Cloudflare Pages会自动：
1. 检测到GitHub仓库更新
2. 拉取最新代码
3. 部署新版本
4. 更新网站内容

---

## 📊 部署检查清单

- [ ] GitHub仓库已创建并推送代码
- [ ] Cloudflare Pages项目已创建
- [ ] 构建设置正确（无构建命令，根目录输出）
- [ ] 首次部署成功
- [ ] 可以访问部署的URL
- [ ] 测试所有功能是否正常

---

## 🐛 常见问题

### Q1: 部署后页面无法显示？
**A**: 检查文件名是否正确，确保是 `行程问题可视化.html` 或创建 `index.html` 作为重定向。

### Q2: 404错误？
**A**: 确保构建输出目录设置为 `/` (根目录)。

### Q3: 如何更新网站？
**A**:
```bash
git add .
git commit -m "更新描述"
git push origin main
```
Cloudflare Pages会自动部署。

### Q4: 本地存储的数据在云端能用吗？
**A**: 可以，LocalStorage在客户端浏览器运行，与部署方式无关。

---

## 📈 性能优化建议

Cloudflare Pages自动优化：
- ✅ 全球CDN分发
- ✅ 自动压缩
- ✅ HTTP/3支持
- ✅ 自动HTTPS

本项目已优化：
- ✅ 单文件应用（减少请求）
- ✅ 纯HTML/CSS/JS（无构建时间）
- ✅ Canvas动画（高性能）

---

## 🔗 相关链接

- **GitHub仓库**: https://github.com/boing1002/math-motion-visualizer
- **Cloudflare Pages文档**: https://developers.cloudflare.com/pages/
- **Wrangler CLI文档**: https://developers.cloudflare.com/workers/wrangler/

---

## ✅ 部署成功后

你的同事可以通过以下链接访问：

```
主链接: https://math-motion-visualizer.pages.dev
GitHub: https://github.com/boing1002/math-motion-visualizer
```

**部署完成！** 🎉
