# 发布包使用说明

本包是已经生成的静态网站，无需安装 Node.js、Python、主题或插件。网页版包含首页、简洁导读、完整版、25 个单题页面和来源页，提供 Markdown、整套资料 ZIP 和 BibTeX 下载。公式已预先排版，字体和样式随包附带，无需外部公式服务。

## 1. 解压

解压 `OpenAI数学物理-GitHub-Pages发布包.zip`。解压后的最外层应能看到 `index.html`、`README.md`、`.nojekyll`、`assets`、`problems` 和 `downloads`。

可以先双击 `index.html` 在电脑浏览器中阅读。网站全部使用相对路径，上传后无需填写 GitHub 用户名，也不必修改文件内容。

## 2. 创建 GitHub 仓库

登录 GitHub → 右上角 `+` → `New repository`。

- 仓库名称建议：`math-physics-notes`。
- 可见性选择：`Public`。
- 可勾选 `Add README`，创建后用包内 README 替换。
- 点击 `Create repository`。

免费账户的公开仓库可使用 GitHub Pages。不要选择不熟悉的额外模板或构建工具。

## 3. 上传解压后的内容

仓库首页 → `Add file` → `Upload files`，将解压目录里面的全部文件和三个文件夹一起拖入上传区域，保持目录结构。提交到 `main` 分支；若页面要求先建立分支和 Pull Request，需要合并后文件才会进入 `main`。

**上传的是解压后的内容，不是 ZIP 文件，也不是包含这些内容的外层文件夹。** 完成后，仓库首页应直接显示 `index.html`。`.nojekyll` 是空文件；若系统隐藏了它，请在资源管理器中开启显示隐藏项目，或在 GitHub 使用 `Add file → Create new file` 创建同名空文件。

所有文件都远小于 GitHub 网页上传的单文件限制，整个发布包也少于一次上传的 100 个文件上限。如浏览器无法拖入文件夹，可按文件夹分别上传，保留名称和层级。

## 4. 开启网页

进入 `Settings → Pages`，在 `Build and deployment` 下设置：

| 项目 | 值 |
|---|---|
| Source | Deploy from a branch |
| Branch | main |
| Folder | / (root) |

点击 `Save`。等待部署完成，以 Pages 页面实际显示的地址为准。也可以在 `Actions` 标签查看部署状态。首次发布或后续更新可能需要数分钟。

例如用户名为 `zhangsan`、仓库名为 `math-physics-notes`，网址通常是：

```text
https://zhangsan.github.io/math-physics-notes/
```

这里的用户名只是示例，本包没有创建远程仓库，也没有替你发布网站。

## 5. 放入公众号

复制部署后的真实网页地址，在公众号文末放置该地址或由它生成的二维码。不要使用电脑本地路径、临时预览地址或本说明中的示例网址。

可直接使用以下文案：

> 完整版资料：25 个数学物理问题的背景、稿件结论、适用条件与潜在研究意义。扫描下方二维码在线阅读，页面同时提供 Markdown 源文件、整套资料和参考文献下载。

发布前在手机微信中测试首页、一个含公式的单题页面和资料下载。如果微信内置浏览器不便下载，可提示读者复制地址到系统浏览器打开。实际网络可达性请在自己的阅读环境中确认。

## 6. 后续更新

- `downloads/` 保存原始 Markdown 与文献库，内部相对链接完整保留。
- `full.html`、`intro.html`、`sources.html`、`problems/*.html` 是对应阅读页面。
- 本包采用预生成网页：只修改 Markdown 不会自动更新 HTML，需要重新生成对应页面和资料 ZIP，再上传替换。
- 不改仓库名和文件路径，通常可继续使用原有阅读地址。
- 原稿验证状态说明、资料版本和非官方解读标识已经保留。本文资料不包含原论文 PDF，仅链接原始来源。

## 常见问题

**看到 404：**检查部署是否完成、Pages 是否选择 `main / (root)`、仓库根目录是否存在小写 `index.html`。

**网页有文字但没有样式或公式字体：**检查 `assets/` 是否完整上传，尤其 `assets/katex/fonts/`。

**下载按钮失效：**检查 `downloads/` 是否完整上传，尤其 `complete-notes.zip`；文件名大小写和中文名称需保持一致。

**仓库显示源码而非阅读网页：**请分享 Pages 提供的 `github.io` 地址，而不是仓库的 `github.com` 地址。

## 官方操作参考

- [GitHub：上传文件](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)
- [GitHub Pages：配置发布来源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [GitHub Pages：快速入门](https://docs.github.com/en/pages/quickstart)
