# GitHub Profile README

这是 `beginner` 的 GitHub 个人主页配置仓库。

## 📁 仓库结构

```
.
├── README.md                      # 主页内容(GitHub 会自动展示)
└── .github
    └── workflows
        └── snake.yml              # 自动生成贡献蛇动画的 Action
```

## 🚀 使用步骤

### 1. 创建同名仓库
在 GitHub 上新建一个**与你用户名完全同名**的仓库 `beginner`(必须是 public)。
将本目录内容推送到该仓库的 `main` 分支即可,GitHub 会自动把 `README.md` 显示在你的个人主页上。

```bash
git init
git add .
git commit -m "feat: add GitHub profile README"
git branch -M main
git remote add origin https://github.com/beginner/beginner.git
git push -u origin main
```

### 2. 启用贡献蛇动画
仓库推送后:
1. 进入仓库 **Actions** 标签页
2. 左侧选择 **Generate Snake** 工作流
3. 点击 **Run workflow** 手动跑一次
4. 等它跑完会自动创建 `output` 分支,贡献蛇就会动起来

之后它会每天自动刷新一次。

## ✏️ 自定义

- **联系链接**:把 README 底部的邮箱 / Twitter / LinkedIn / Telegram 链接换成你自己的
- **技术栈**:增删对应语言的 `img.shields.io` 徽章即可
- **简介信息**:修改顶部的 `developer` 对象和打字机标题里的文字
- **配色**:当前主题是 `radical` + 青色 `#00D9FF`,可换成 `tokyonight`、`dracula`、`vue` 等

> 💡 使用前请把 README 中所有的 `beginner` 占位用户名替换成你的实际用户名(如果你不是叫 beginner)。
