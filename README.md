# JTBD 报告部署项目

用于托管 JTBD 需求分析报告的静态站点。

## 部署到 Vercel

### 方式 1：Git 部署（推荐）

1. **创建 GitHub 仓库**
   ```bash
   cd /home/admin/.openclaw/projects/CLAW-multi-agent-system/jtbd-vercel-deploy
   git init
   git add .
   git commit -m "Initial commit: JTBD reports"
   # 然后在 GitHub 创建空仓库，按提示推送
   ```

2. **在 Vercel 导入项目**
   - 访问 [vercel.com](https://vercel.com) 并登录
   - 点击 "Add New Project"
   - 选择 "Import Git Repository"
   - 选择你刚创建的 GitHub 仓库
   - 点击 "Deploy"

3. **完成！**
   - Vercel 会自动分配域名：`https://your-project.vercel.app`
   - 报告访问路径：`https://your-project.vercel.app/reports/银发育儿项目.html`

### 方式 2：Vercel CLI 部署

1. **安装 Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **登录 Vercel**
   ```bash
   vercel login
   ```

3. **部署**
   ```bash
   cd /home/admin/.openclaw/projects/CLAW-multi-agent-system/jtbd-vercel-deploy
   vercel --prod
   ```

### 方式 3：手动拖拽部署（最简单）

1. 访问 [vercel.com/new](https://vercel.com/new)
2. 创建项目后，在项目页面找到 "Deploy" 选项
3. 直接把 `jtbd-vercel-deploy` 文件夹拖拽到上传区域
4. 完成！

---

## 项目结构

```
jtbd-vercel-deploy/
├── reports/              # 报告文件目录
│   ├── 银发育儿项目.html
│   └── [更多报告...]
├── vercel.json           # Vercel 配置
└── README.md
```

## 添加新报告

只需把新生成的 HTML 报告放到 `reports/` 目录，然后重新部署即可。

## 访问示例

- 主页：`https://your-domain.vercel.app/`
- 报告：`https://your-domain.vercel.app/reports/银发育儿项目.html`
