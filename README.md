# Xu Zhu · Academic Homepage

英文个人学术主页，内容根据 2026 年 11 月提供的 CV 整理。纯 HTML / CSS，无需安装依赖或构建，可直接由 GitHub Pages 发布。

## 文件位置

- `index.html`：个人介绍、论文状态、教育和项目等全部内容。
- `assets/styles.css`：布局、配色和手机适配。
- `assets/Curriculum_Vitae.pdf`：主页上可下载的原始 CV（含原 CV 中的联系方式）。
- `assets/favicon.svg`：浏览器标签页图标。

## 本地预览

直接用浏览器打开 `index.html` 即可。如果已安装 Python，也可在本目录运行 `python -m http.server 8000`，然后访问 http://localhost:8000 。

## 添加照片

将照片保存为 `assets/profile.jpg`，在 `index.html` 中找到 `<figure class="portrait" ...>`，将其中的 `<span>Photo</span>` 替换成：

```html
<img src="assets/profile.jpg" alt="Portrait of Xu Zhu" width="180" height="180">
```

## 日常更新

在本目录打开终端，先确认没有未保存的改动，再同步远程：

```powershell
git status
git pull --ff-only origin main
```

编辑对应文件并检查页面，再保存本地版本：

```powershell
git add index.html assets README.md .gitignore .nojekyll
git commit -m "Update academic homepage"
```

确认要更新线上主页时执行：

```powershell
git push origin main
```

推送需要你有该仓库写入权限。若 GitHub Pages 已设置为从 `main` 分支的根目录发布，推送后会自动更新。否则到仓库 Settings → Pages → Build and deployment，选择 Deploy from a branch → main → / (root)。发布进度可在仓库 Actions 查看。

线上地址：https://pgsun02.github.io/

## 内容维护提示

- 所有论文的署名角色和状态来自提供的 CV；未添加未经提供的完整作者表、导师、论文链接或代码链接。
- `RecompileAgent` 标题中的 `Binar` 按原 CV 保留，请核对正式标题后同步修改。
- 论文录用或发表后，在 `index.html` 更新状态、年份和正式链接；同时更新 CV 及页脚日期。
- 2027 年 6 月为预计毕业时间，当前学位表述为在读。
- 默认照片是空白占位，不会请求不存在的图片。
