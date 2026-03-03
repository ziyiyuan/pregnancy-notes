# 孕期记录

本仓库用于记录和管理孕期相关事宜，使用 MkDocs + Material 主题构建为在线文档。

**在线访问**：<https://ziyiyuan.github.io/pregnancy-notes/>

---

## 目录结构

| 路径 | 说明 |
|------|------|
| `docs/` | 文档源目录（MkDocs 使用） |
| `docs/index.md` | 首页：基本信息、孕周、本「书」目录 |
| `docs/待产包准备/` | 北医三院产科入院清单及配图 |
| `docs/孕期生活/` | 孕期菜单等 |
| `mkdocs.yml` | MkDocs 配置（导航、主题、站点 URL） |
| `requirements-docs.txt` | 构建依赖（mkdocs、mkdocs-material） |
| `dates.json` | 本地用日期数据（LMP、EDD 等） |

---

## 本地预览

```bash
pip install -r requirements-docs.txt
mkdocs serve
```

浏览器打开 http://127.0.0.1:8000 预览。

---

## 发布（GitHub Pages）

- 推送代码到 `main` 或 `master` 分支后，**GitHub Actions** 会自动构建并部署到 GitHub Pages。
- 仓库 **Settings → Pages** 中需将 **Source** 设为 **GitHub Actions**。
- 部署完成后访问：`https://<用户名>.github.io/pregnancy-notes/`（或你实际仓库名）。

无需本地执行 `mkdocs gh-deploy`。

---

## 可选配置

- 在 `mkdocs.yml` 中填写 `repo_url`（仓库地址），页脚会显示「在 GitHub 上编辑」等链接。
- `dates.json` 供本地脚本或笔记使用，不参与站点构建。
