# GitHub Profile README

这是 `beginner-wj` 的 GitHub 个人主页配置仓库。

## 📁 仓库结构

```
.
├── README.md                      # 主页内容(GitHub 会自动展示)
└── .github
    └── workflows
        └── snake.yml              # 自动生成贡献蛇动画的 Action
```

## 🚀 使用步骤

### 1. 创建同名仓库(关键!)
在 GitHub 上新建一个**与你用户名完全同名**的仓库 `beginner-wj`(必须是 public)。

> ⚠️ GitHub 个人主页的 README 只会在「与用户名同名的仓库」里展示。
> 也就是说这个 README **必须**放在名为 `beginner-wj` 的仓库,放在 `wj-alarm`、`github-ui` 这类仓库里是不会出现在你的个人主页的。

将本目录内容推送到该仓库的 `main` 分支即可:

```bash
git init -b main
git add .
git commit -m "feat: add GitHub profile README"
git remote add origin https://github.com/beginner-wj/beginner-wj.git
git push -u origin main
```

### 2. 推送失败 / 连接被重置怎么办?
如果你看到 `fatal: ... Connection was reset` 或 `unable to access`,基本是**网络无法直连 GitHub** 导致的(国内常见)。解决办法任选其一:

**方案 A:给 git 配代理(推荐,如果你开了科学上网)**
```bash
# 把 7890 换成你代理软件实际的端口号(Clash 默认 7890,v2rayN 默认 10809)
git config --global http.proxy http://127.0.0.1:7890
git config --global https.proxy http://127.0.0.1:7890
```
推送成功后如果不想一直走代理,可取消:
```bash
git config --global --unset http.proxy
git config --global --unset https.proxy
```

**方案 B:改用 SSH 方式推送**
```bash
git remote set-url origin git@github.com:beginner-wj/beginner-wj.git
git push -u origin main
```
(需要先在 GitHub 配好 SSH key)

**方案 C:用 SSH over 443 端口**(连 22 端口被封时可用)
```bash
# 在 ~/.ssh/config 加入:
#   Host github.com
#       Hostname ssh.github.com
#       Port 443
#       User git
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

> 💡 使用前请确认 README 中的用户名 `beginner-wj` 与你的实际用户名一致。
