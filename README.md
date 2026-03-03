# 孕期记录

本仓库用于记录和管理孕期相关事宜。

## 基本信息

| 项目 | 日期 |
|------|------|
| **末次月经 (LMP)** | 2025-08-28 |
| **预产期 (EDD)** | 2026-06-04（按 Naegele 法则：LMP + 280 天）|

## 当前孕周（截至 2026-03-03）

- **孕周**：26 周 + 6 天（26w6d）
- **孕龄**：约 188 天

## 目录说明

- `README.md` — 本说明与关键日期
- `待产包准备/` — 北医三院产科入院清单等（可同步到 Book）
- `notes/` — 孕期笔记、产检记录等（可自建）
- `docs/` — 用于发布为在线 Book 的文档源（MkDocs）

---

## 发布为 Book（在线文档）

本项目可用 **MkDocs + Material 主题** 构建为在线「书」，支持侧栏目录、搜索、深浅色切换。

### 本地预览

```bash
pip install -r requirements-docs.txt
mkdocs serve
```

浏览器打开 http://127.0.0.1:8000 即可预览。

### 部署到 Git 并发布

1. **初始化仓库并推送到远程（若尚未）**
   ```bash
   git init
   git add .
   git commit -m "孕期记录与待产包清单"
   git remote add origin <你的仓库地址>   # 如 https://github.com/用户名/pg.git
   git push -u origin main
   ```

2. **发布为 GitHub Pages（Book 在线版）**
   ```bash
   pip install -r requirements-docs.txt
   mkdocs gh-deploy
   ```
   首次会要求 Git 授权；完成后页面地址为：`https://<用户名>.github.io/<仓库名>/`。

3. **在 `mkdocs.yml` 中填写 `repo_url`**（可选），便于页面上显示「编辑/仓库」链接。

**注意**：更新清单后，若希望在线 Book 同步，需把 `待产包准备/北医三院产科入院清单.md` 的修改复制到 `docs/待产包准备/北医三院产科入院清单.md`，再执行 `mkdocs gh-deploy`。
