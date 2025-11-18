# SOP: Technical Writing Workflow

**Overview:**

从写 Markdown 文档到发布成网站的完整流程。

包含文档生成、版本控制、协作、托管和工具使用说明。

## 一、工作流程概览

1. Markdown 文档 → 放入 docs/ 文件夹

2. docs.yml 中添加导航 → 定义网站结构

3. 本地预览 → 使用 mkdocs serve 生成网站预览

4. 版本管理 → 提交到 GitHub 仓库

5. 发布网站 → GitHub Pages 自动生成线上文档

	Markdown（文档内容）

	↓

	MkDocs（自动生成结构化网站）

	↓

	GitHub Pages（线上发布）

## 二、版本控制
### Git + GitHub
- 仓库地址： https://github.com/LumosYip/my-techwriting-portfolio
- 说明：
	- 所有文档使用 Git 进行版本管理
	- 使用 Pull Request 进行协作和审核
	
---

## 三、文档生成

1. 项目结构示例

		my-docs/
		├─ mkdocs.yml                    ← 
		└─ docs/
			├─ index.md                  ← 首页
			│
			├─ writing/                  ← 技术写作区
			│   ├─ tw-overview.md        ← 技术写作是什么
			│   ├─ workflow.md           ← TW工作流程
			│   └─ version-control.md    ← Git/GitHub指南
			│
			├─ translation/              ← 翻译 & CAT 工具区
			│   ├─ cat-overview.md
			│   ├─ matecat.md
			│   └─ localization-tips.md  ← 软件本地化技巧
			│
			├─ forensics/                ← 业务文档区（如取证类文档）
			│   ├─ drone-forensics.md
			│   └─ mobile-forensics.md
			│
			└─ tools/                    ← 环境、工具、软件教程
				├─ markdown-tools.md     ← 写作习惯
				└─ mkdocs-guide.md       ← MkDocs如何安装、serve、发布


2. MkDocs / Docusaurus

	**本地运行 MkDocs**

	- 用 MkDocs 在本地创建、编辑并预览文档网站
	- 目的：
		- 使用 Markdown 编写说明书、用户手册、知识库
		- 自动生成清晰的静态网站

---

3. 操作步骤

（1）安装 MkDocs

`pip install mkdocs`

- 在命令行执行安装
	
- 安装 MkDocs 工具，让系统支持 mkdocs 命令（就像给电脑装上“文档网站生成器”）

（2）创建新项目

`mkdocs new my-docs`

- 标准项目结构：

		my-docs/
			├─ mkdocs.yml ← 网站配置文件
			└─ docs/
			└─ index.md ← 首页内容

（3）进入项目目录

`cd my-docs`

- 所有 MkDocs 命令必须在项目目录内运行

（4）启动本地预览

`mkdocs serve`

- 注：进入目录： `C:\users\12857\my-docs` 后运行

- 浏览器访问：http://127.0.0.1:8000/

- 自动监控文件变化并重新加载页面

（5）编辑首页文档 `index.md`

- 路径：`c:\users\12857\my-docs\docs\index.md`

- 用 Markdown 编写首页内容，自动渲染为网页

（6）修改配置文件 `mkdocs.yml`

- 控制网站导航栏结构

- 示例：

		site_name: Lumos's Docs
		theme:
			name: material
		nav: #导航栏
		- Homepage: index.md  #主页对应文档
		- Writing: Working Procedures of Technical Writing (TW).md  #其他文档
		- Translation: Computer-Aided Translation (CAT).md
		
- 注意：Material 主题需要单独安装

（7）新建文档

- 在项目文件内新建 `.md` 文档，如：*Writing*、*Translation*、用户手册、FAQ等

---

## 四、本地与在线工具

**本地工具**

- Notepad++
- MarkdownViewer++（可实时预览 / 导出 HTML、PDF）
	- 下载：https://www.cnblogs.com/keping/p/14152251.html

**在线工具**

- Markdown 编辑 + 预览一体工具
	- 链接：https://markdown.com.cn/editor/

---

## 五、托管与发布

- GitHub Pages 自动发布网站

- 版本控制由 Git + GitHub 管理

---

## 六、协作与审核

- 使用 GitHub Pull Request 进行协作

- 使用 GitHub Issues 记录问题和讨论

---

## 七、编写工具

- VS Code

- Typora
	

