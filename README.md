# 瓶颈理论选股仪表盘

> 🦊 Serenity Chokepoint Theory Dashboard  
> 分析框架：白毛股神 @aleabitoreddit 瓶颈理论

## 📡 在线访问

部署到 GitHub Pages 后：`https://你的用户名.github.io/stock-dashboard/`

## 🚀 快速部署（3 步）

### 1. 安装 Git
下载安装：https://git-scm.com/download/win

### 2. 创建 GitHub 仓库
```
在 GitHub 上新建仓库 → 命名 stock-dashboard → 设为 Public
不要勾选 "Add a README file"
```

### 3. 推送代码
```bash
cd C:\Users\zmq\.easyclaw\workspace\output\dashboard-repo

git init
git add .
git commit -m "v1.0 初始部署"

# 关联你的仓库（替换为你的用户名）
git remote add origin https://github.com/你的用户名/stock-dashboard.git
git branch -M main
git push -u origin main
```

### 4. 开启 GitHub Pages
```
仓库 → Settings → Pages →
  Source: Deploy from a branch
  Branch: main / root
  → Save

等 1-2 分钟 → 访问 https://你的用户名.github.io/stock-dashboard/
```

## 🔄 后续更新

每次仪表盘数据更新后：

```bash
cd C:\Users\zmq\.easyclaw\workspace\output\dashboard-repo

# 复制最新文件
copy ..\dashboard\dashboard.html index.html /Y
copy ..\dashboard\r*.html reports\ /Y

# 推送
git add . && git commit -m "更新 $(Get-Date -Format 'yyyy-MM-dd HH:mm')" && git push
```

## 📂 文件结构
```
stock-dashboard/
  index.html          ← 主仪表盘
  reports/            ← 分析报告 HTML
    r001_安集科技688019.html
    r002_人形机器人赛道选股.html
    ...
```

---

**拉布布会在每次分析完成后自动更新 index.html 并推送。**
