# GB-CMS 帮助文档

这是 GB-CMS 信令服务器的静态帮助文档和 API 文档站点。

## 目录结构

- `index.html`: 首页
- `api_docs.html`: API 文档页面
- `style.css`: 样式文件
- `wrangler.toml`: Cloudflare Pages 配置文件
- `_headers`: Cloudflare Pages 响应头配置

## 部署到 Cloudflare Pages

### 方法 1: 连接 Git 仓库 (推荐)

1. 将此项目推送到 GitHub/GitLab。
2. 登录 Cloudflare Dashboard，进入 **Workers & Pages**。
3. 点击 **Create application** -> **Pages** -> **Connect to Git**。
4. 选择你的仓库。
5. 在 **Build settings** 中：
   - **Framework preset**: None
   - **Build command**: (留空)
   - **Build output directory**: `.` (或者留空，默认为根目录)
6. 点击 **Save and Deploy**。

### 方法 2: 使用 Wrangler CLI 直接上传

如果你安装了 Node.js，可以使用 Wrangler 命令行工具直接部署：

```bash
# 安装依赖 (如果尚未安装)
npm install -g wrangler

# 登录 Cloudflare
wrangler login

# 部署当前目录
wrangler pages deploy . --project-name gb-cms-helppage
```


## 本地预览

如果你安装了 Wrangler，可以在本地预览：

```bash
wrangler pages dev .
```
