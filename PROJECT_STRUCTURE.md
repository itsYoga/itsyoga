# 專案結構指南 / Project Structure Guide

## 📁 專案組織說明 / Project Organization

您的個人網站專案現在已經重新組織，結構清晰且易於維護。

### 🗂️ 目錄結構 / Directory Structure

```
itsyoga/
├── 📄 docs/                    # 🌐 網站檔案 - GitHub Pages 部署
│   ├── index.html             # 主要網站頁面
│   ├── Resume.pdf             # 履歷 PDF 版本
│   └── Resume_alt.pdf         # 備選履歷 PDF 版本
│
├── 📝 resume/                 # ✏️ 履歷源文件和編譯工具
│   ├── Resume.tex             # 主要履歷 LaTeX 源文件
│   ├── Resume_alt.tex         # 備選履歷 LaTeX 源文件
│   ├── Makefile               # 自動編譯命令
│   ├── compile.sh             # 編譯輔助腳本
│   └── latexmkrc              # LaTeX 配置
│
├── 📖 README.md               # 專案說明文檔
├── 🔧 .gitignore              # Git 忽略規則
└── 📘 RENAME_GUIDE.md        # 重新命名指南
```

---

## 🎯 各部分用途 / Purpose of Each Section

### 1. 📄 `docs/` - 網站檔案 / Website Files
- **用途**: 包含要部署到 GitHub Pages 的網站檔案
- **內容**: HTML 網頁、PDF 履歷檔案
- **自動部署**: 推送到 GitHub 後會自動部署到網站

### 2. 📝 `resume/` - 履歷源文件 / Resume Source Files
- **用途**: 履歷的 LaTeX 源文件和編譯工具
- **工作流程**: 編輯 → 編譯 → 自動複製到 `docs/`

---

## 🚀 使用方法 / Usage

### 📝 編譯履歷 / Compile Resume

```bash
# 進入履歷目錄
cd resume

# 編譯備選履歷（會自動複製到 docs/）
make resume-alt

# 或使用自動監視模式（檔案變化時自動編譯）
make watch

# 使用腳本自動編譯
./compile.sh
```

### 🧹 清理臨時文件 / Clean Temp Files

```bash
cd resume

# 清理 LaTeX 臨時文件
make clean

# 清理所有文件（包括 PDF）
make clean-all
```

---

## ✨ 優勢 / Benefits

### ✅ 清晰分離
- 履歷源文件與網站部署檔案分開
- 易於維護和管理

### ✅ 自動化
- 編譯後自動複製 PDF 到 `docs/`
- 網站自動使用最新的履歷

### ✅ 版本控制
- 源文件（.tex）有版本控制
- 生成的 PDF 自動同步到網站

---

## 📋 工作流程 / Workflow

### 編輯履歷 / Editing Resume

1. 編輯 `resume/Resume_alt.tex`
2. 編譯：`cd resume && make resume-alt`
3. PDF 自動複製到 `docs/`
4. 推送到 GitHub：`git push`
5. 網站自動更新！

### 更新網站內容 / Updating Website

1. 編輯 `docs/index.html`
2. 推送到 GitHub：`git push`
3. 網站自動更新！

---

## 🎨 未來擴展 / Future Expansion

您可以在 `docs/` 中添加更多網站內容：
- 📂 `docs/css/` - 樣式文件
- 📂 `docs/js/` - JavaScript 文件
- 📂 `docs/images/` - 圖片資源
- 📂 `docs/projects/` - 專案展示頁面

---

## ⚙️ 配置說明 / Configuration

### GitHub Pages 設置
1. 前往設定 → Pages
2. 選擇分支：`main`
3. 選擇文件夾：`/docs`
4. 保存

您的網站將在幾分鐘內於以下地址可用：
- `https://itsyoga.github.io`

---

## 📞 協助 / Help

如有問題，請參考：
- `README.md` - 完整使用說明
- `RENAME_GUIDE.md` - 重新命名指南

