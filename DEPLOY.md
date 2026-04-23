# GitHub Pages 部署指南

## 📁 文件结构

```
github-pages/
├── index.html              # 主页
├── privacy-policy.html     # 隐私政策
└── terms-of-service.html  # 服务条款
```

## 🚀 部署步骤

### 方式一：创建新仓库（推荐）

#### Step 1: 创建新 GitHub 仓库

1. 登录 GitHub: https://github.com
2. 点击右上角 **"+"** → **"New repository"**
3. 填写仓库信息：
   - **Repository name**: `tiktok-name-generator-privacy`
   - **Description**: `TikTokアカウント名生成ツール プライバシーポリシー＆利用規約`
   - **Visibility**: `Public`（必须公开才能使用 GitHub Pages）
4. 点击 **"Create repository"**

#### Step 2: 上传文件

在仓库页面，点击 **"uploading an existing file"**，然后上传这3个文件：
- `index.html`
- `privacy-policy.html`
- `terms-of-service.html`

#### Step 3: 启用 GitHub Pages

1. 进入仓库的 **Settings**（设置）
2. 左侧菜单找到 **"Pages"**
3. **Source** 部分：
   - 选择 **"Deploy from a branch"**
   - Branch 选择 **"main"** / **"master"**
   - Folder 选择 **"/ (root)"**
4. 点击 **"Save"**

#### Step 4: 等待部署

等待 1-2 分钟，GitHub 会自动部署。

#### Step 5: 获取 URL

部署完成后，你的页面 URL 将是：
```
https://你的用户名.github.io/tiktok-name-generator-privacy/
```

---

### 方式二：添加到现有项目仓库

如果你已经有项目仓库，可以将文件添加到现有仓库中：

```bash
# 克隆你的仓库
git clone https://github.com/你的用户名/你的仓库名.git
cd 你的仓库名

# 创建 docs 文件夹（如果不存在）
mkdir -p docs

# 复制文件到 docs 文件夹
cp /path/to/github-pages/*.html docs/

# 提交并推送
git add .
git commit -m "Add privacy policy and terms of service"
git push origin main

# 在 GitHub Settings → Pages 中启用
# Source 选择 "Deploy from a branch"
# Branch 选择 "main", Folder 选择 "/docs"
```

部署 URL 将是：
```
https://你的用户名.github.io/你的仓库名/
```

---

## ✅ 部署完成后

### 验证部署

1. 访问你的 GitHub Pages URL
2. 确认页面正常显示
3. 点击链接测试页面跳转

### 获取 TikTok 审核所需的 URL

| 页面 | URL 格式 |
|------|---------|
| 首页 | `https://用户名.github.io/tiktok-name-generator-privacy/` |
| 隐私政策 | `https://用户名.github.io/tiktok-name-generator-privacy/privacy-policy.html` |
| 服务条款 | `https://用户名.github.io/tiktok-name-generator-privacy/terms-of-service.html` |

---

## 🔧 自定义域名（可选）

如果你有自己的域名，可以配置自定义域名：

1. 在仓库 **Settings → Pages** 中
2. **Custom domain** 输入你的域名
3. 在你的域名 DNS 设置中添加：
   - CNAME 记录指向 `你的用户名.github.io`

---

## ❓ 常见问题

**Q: 页面显示 404？**
A: 等待 2-5 分钟，GitHub Pages 需要时间部署。确认仓库是 Public。

**Q: 样式丢失？**
A: 确保 CSS 中的路径是相对路径。

**Q: 图片不显示？**
A: 如果有图片，使用绝对路径或上传到仓库。

---

## 📝 下一步

部署完成后，在 TikTok 开发者平台填写：
- **隐私政策 URL**: `https://用户名.github.io/tiktok-name-generator-privacy/privacy-policy.html`
- **服务条款 URL**: `https://用户名.github.io/tiktok-name-generator-privacy/terms-of-service.html`
