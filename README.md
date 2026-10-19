# 严海涛 · 个人学术主页

版本：v1.1（2026-10-19）

一份可直接托管到 GitHub Pages 的静态个人主页。纸白、墨绿与朱砂色，配合原创山形曲线、圆相与中文衬线排版。无需构建工具、数据库、付费服务或外部字体。

## 文件结构

- `index.html`：个人简介、研究与项目、教育、工作经历和兴趣
- `styles.css`：颜色、布局、响应式、打印与减少动态效果设置
- `script.js`：手机导航与当前阅读章节提示；禁用 JavaScript 后仍可阅读与导航
- `assets/favicon.svg`：原创站点图标
- `.nojekyll`：让 GitHub Pages 直接提供静态文件

## 本地预览

直接打开 `index.html` 即可。需要通过本地 HTTP 预览时，可在此目录运行：

```bash
python3 -m http.server 8000
```

随后访问 `http://localhost:8000`。这只是可选预览方式，不是网站运行依赖。

## 免费部署到 GitHub Pages

GitHub Free 支持公开仓库的 GitHub Pages。网站以及公开仓库中的源文件都可被他人访问；上传前请确认个人资料适合公开。默认 `github.io` 域名不需要购买域名。

1. 使用已经创建的公开仓库 [`HaiTaoYan-NanKai/Curriculum-Vitae`](https://github.com/HaiTaoYan-NanKai/Curriculum-Vitae)。
2. 将本目录内的全部文件放入仓库根目录，并提交到 `main` 分支。应直接看到 `index.html`，不要将整个外层文件夹再嵌套一层。保留 `.nojekyll` 文件；网页上传未包含该隐藏文件时，可在 GitHub 使用 Add file → Create new file 创建同名空文件。
3. 打开仓库 **Settings → Pages**。
4. 在 **Build and deployment → Source** 选择 **Deploy from a branch**。
5. 选择 **main** 分支和 **/ (root)**，然后保存。
6. 在 Actions 查看部署运行结果，等待 Pages 设置页显示站点地址，再打开检查。

此项目部署后的预期地址为 `https://haitaoyan-nankai.github.io/Curriculum-Vitae/`，这不代表已经上线；请以 Pages 显示的实际地址为准。本项目所有资源使用相对路径，可以在这个项目子路径正常加载。

以后修改文件并提交到发布分支，就会触发更新。仓库 Pages 设置和 GitHub 的访问限制以实际账号状态为准。

官方说明（2026-10-19 核对）：
- [配置 GitHub Pages 发布来源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [创建 GitHub Pages 站点](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)

## 修改内容

在 `index.html` 搜索对应标题即可找到内容：

- `id="about"`：简介与基础信息
- `id="research"`：研究与项目
- `id="education"`：教育经历
- `id="experience"`：工作经历
- `id="life"`：兴趣

博士阶段使用“在读”和“预计 2028.06”，请随实际情况维护。题目以“研究与项目”展示；Cheeger 相关工作附有本人提供的 [ResearchGate 论文链接](https://www.researchgate.net/publication/357789830_Cheeger_Inequalities_for_the_Discrete_Magnetic_Laplacian)。期刊、年份、作者、摘要、代码与 DOI 尚未提供，因此不做补写。新增论文或项目资料时，请只添加已确认的信息和真实链接。

页脚公开联系邮箱为 `huet-iset@outlook.com`，使用 `mailto:` 链接。未添加未经确认的其他联系方式、照片或论文下载文件。邮箱与 ResearchGate 论文链接均由本人提供用于主页展示。修改邮箱时，记得同时修改显示文字与 `mailto:` 地址。

### 改颜色与字体

在 `styles.css` 顶部的 `:root` 修改 `--paper`、`--ink`、`--jade` 和 `--red`。改变文字颜色时请保持可读的对比度。

字体使用访客设备已有的中文字体，优先宋体风格标题与清晰的无衬线正文，离线也能显示。不同系统的字形会略有差异；不加载第三方字体服务或追踪脚本。

### 新增链接与资料

站内文件使用 `./assets/文件名` 等相对路径，避免以 `/` 开头，这样普通项目仓库也能正确显示。加入 PDF 等资料前，先确认作者权利、公开权限和个人隐私。

## 可访问性与隐私

- 语义化章节、单一主标题、跳转至主要内容链接
- 键盘可操作的手机导航，支持 Escape 关闭并恢复焦点
- 移动端适配与系统“减少动态效果”偏好
- 页面无统计追踪、无 Cookie、无表单数据收集、无外部资源依赖；点击 ResearchGate 论文链接后会进入第三方网站
- 提供打印样式

出生年月、籍贯、居住城市等资料均会显示在网页中。若之后不希望继续公开，请修改页面；公开 Git 历史也可能保留旧版本。

## 发布状态

此交付是网站源文件。是否已推送、是否已启用 Pages、最终网址及在线部署结果，需要以实际 GitHub 仓库为准。
