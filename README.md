# 陈灵娜艺术家网站使用指南

## 📁 文件结构

```
lingna-chen-website/
├── index.html          # 主页（作品展示）
├── about.html          # 关于页面
├── exhibitions.html    # 展览和CV页面
├── work1.html          # 作品详情页模板
├── assets/             # 样式和脚本文件（保持不变）
├── images/             # 图片文件夹
└── README.md           # 本说明文档
```

## 🎨 如何更新内容

### 1️⃣ 更新主页作品（index.html）

在 `index.html` 中找到作品部分，修改以下内容：

```html
<h2><a href="work1.html">作品标题 1<br />
Work Title 1</a></h2>
<p>在这里添加你的作品描述...</p>
```

- 替换 "作品标题" 为你的实际作品名称
- 替换作品描述
- 修改年份（`<span class="date">2024</span>`）
- 更换图片（`<img src="images/pic01.jpg"`）

### 2️⃣ 添加新作品

1. 复制 `work1.html` 文件
2. 重命名为 `work2.html`, `work3.html` 等
3. 编辑文件内容：
   - 修改标题
   - 替换作品描述
   - 更新作品信息（媒介、尺寸、年份）
   - 更换图片路径

### 3️⃣ 更新关于页面（about.html）

在 `about.html` 中填写：
- 艺术家陈述
- 个人简介
- 创作实践描述
- 教育背景

### 4️⃣ 更新展览信息（exhibitions.html）

在 `exhibitions.html` 中添加：
- 个展信息
- 群展信息
- 获奖记录
- 教育背景
- 驻留项目
- 出版物

### 5️⃣ 更换图片

1. 将你的作品照片放入 `images/` 文件夹
2. 建议命名：`work1-main.jpg`, `work1-detail1.jpg` 等
3. 在 HTML 中更新图片路径：`<img src="images/你的图片名.jpg">`

**图片建议：**
- 主图尺寸：1920x1080px 左右
- 缩略图：800x600px 左右
- 格式：JPG（照片）或 PNG（带透明背景）
- 文件大小：尽量控制在 500KB 以内（提高加载速度）

## 📧 设置留言表单（Formspree）

当前所有页面的表单中有这行代码：
```html
<form method="POST" action="https://formspree.io/f/YOUR_FORM_ID">
```

### 设置步骤：

1. 访问 https://formspree.io
2. 免费注册账号
3. 创建新表单，使用你的邮箱：`2024chenyaotian@gmail.com`
4. 复制你获得的表单 ID（类似 `mxxxxxxx`）
5. 在所有 HTML 文件中，将 `YOUR_FORM_ID` 替换为你的实际 ID

**替换示例：**
```html
<!-- 之前 -->
<form method="POST" action="https://formspree.io/f/YOUR_FORM_ID">

<!-- 之后 -->
<form method="POST" action="https://formspree.io/f/mxxxxxxx">
```

设置完成后，访客提交表单时，消息会自动发送到你的邮箱。

## 🚀 部署到 GitHub Pages

### 步骤 1: 创建 GitHub 仓库

1. 登录 GitHub (https://github.com)
2. 点击右上角 "+" → "New repository"
3. 仓库名称输入：`lingna-chen.github.io` 或任意名称
4. 选择 "Public"
5. 点击 "Create repository"

### 步骤 2: 上传文件

**方法 A - 网页上传（简单）：**

1. 在你的仓库页面，点击 "Add file" → "Upload files"
2. 拖拽所有文件和文件夹到上传区域
3. 填写提交信息：`Initial commit`
4. 点击 "Commit changes"

**方法 B - Git 命令行（推荐）：**

```bash
# 1. 在本地文件夹中打开终端
git init
git add .
git commit -m "Initial commit"

# 2. 连接到你的 GitHub 仓库
git remote add origin https://github.com/你的用户名/你的仓库名.git

# 3. 推送到 GitHub
git branch -M main
git push -u origin main
```

### 步骤 3: 启用 GitHub Pages

1. 在仓库页面，点击 "Settings"
2. 在左侧菜单找到 "Pages"
3. 在 "Source" 下拉菜单中选择 "main" 分支
4. 点击 "Save"
5. 等待几分钟，你的网站将在以下地址发布：
   - 如果仓库名是 `lingna-chen.github.io`：https://lingna-chen.github.io
   - 其他名称：https://你的用户名.github.io/仓库名

## 🔄 后续更新

### 更新内容：

1. 在本地修改 HTML 文件
2. 上传到 GitHub（重复步骤 2）
3. 网站会自动更新（可能需要几分钟）

### 添加新作品：

1. 复制 `work1.html`，重命名为 `work2.html`
2. 编辑内容
3. 在 `index.html` 中添加新作品的卡片链接
4. 上传新文件到 GitHub

## 📱 社交媒体链接

所有页面已配置你的社交媒体：
- Instagram: @nainwhisper
- 小红书 RedNote: 173550956
- 邮箱: 2024chenyaotian@gmail.com

如需修改，在每个 HTML 文件中搜索对应的链接并替换。

## 🎯 快速检查清单

在发布前，确保：

- [ ] 所有 `YOUR_FORM_ID` 已替换为 Formspree ID
- [ ] 所有作品标题、描述已更新
- [ ] 所有图片已替换为你的作品照片
- [ ] About 页面已填写完整
- [ ] Exhibitions 页面已添加你的展览信息
- [ ] 社交媒体链接正确
- [ ] 联系邮箱正确

## ❓ 常见问题

**Q: 视频如何嵌入？**
A: 在 `work1.html` 中有 YouTube 嵌入示例。上传视频到 YouTube，复制视频 ID，替换示例中的 `VIDEO_ID`。

**Q: 如何添加更多页面？**
A: 复制任意现有页面，修改内容，然后在导航栏（`<nav>`）中添加链接。

**Q: 网站加载慢怎么办？**
A: 压缩图片文件。可以使用在线工具如 TinyPNG (https://tinypng.com)。

**Q: 可以使用自定义域名吗？**
A: 可以！在 GitHub Pages 设置中配置你的域名，并在域名提供商处设置 DNS。

## 📞 需要帮助？

如有问题，可以：
- 查看 HTML5 UP 文档：https://html5up.net
- GitHub Pages 文档：https://docs.github.com/pages
- Formspree 文档：https://help.formspree.io

---

**祝你的艺术网站成功上线！🎨**
