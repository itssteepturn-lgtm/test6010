# A330 题库5389题

纯网页题库：首页直接练习，随机/章节/错题不重复推进，关键词搜索，错题导入导出合并。

进入口令：`1009`（首次正确后会记住）

## 文件说明

| 文件 | 作用 |
|------|------|
| `index.html` | **主程序**。包含全部界面、练习/搜索/错题逻辑，以及 5389 道题数据。打开这个文件就能用。 |
| `manifest.json` | **PWA 清单**。让手机/iPad 浏览器「添加到主屏幕」时显示名称、主题色，并尽量以独立 App 方式打开。 |
| `sw.js` | **Service Worker（离线辅助）**。有网时正常访问；短暂断网时尽量用已缓存内容打开（能力有限，主要靠浏览器缓存）。 |
| `robots.txt` | **防搜索引擎收录**。告诉爬虫不要索引本站。 |
| `README.md` | 本说明文件。 |

> 没有后端、没有数据库。错题和进度存在你设备浏览器的 `localStorage` 里；换设备请用 App 内「同步」导出/导入。

## 本机直接用

1. 下载全部文件，放在同一文件夹。
2. 用浏览器打开 `index.html`。  
   - iPhone/iPad 的 Safari/文件 App 也可以打开。  
   - 若本地打开有限制，可用下面的 GitHub Pages 方式。

## 部署到 GitHub Pages（推荐）

仓库已在 GitHub 时，按下面做即可得到一个网址，手机/iPad 都能打开。

### 方法 A：在网页上设置（最简单）

1. 打开你的仓库页面（例如 `https://github.com/你的用户名/仓库名`）。
2. 确认最新代码已在 `main` 分支（若有 Pull Request，先合并）。
3. 点 **Settings → Pages**。
4. **Build and deployment → Source** 选 **Deploy from a branch**。
5. Branch 选 `main`，文件夹选 `/ (root)`，点 **Save**。
6. 等 1～2 分钟，页面上方会出现访问地址，一般是：
   - `https://你的用户名.github.io/仓库名/`
   - 或 `https://你的用户名.github.io/仓库名/index.html`

### 方法 B：命令行上传后同样开 Pages

```bash
# 若还没有本地仓库，先建空仓库再：
git clone https://github.com/你的用户名/仓库名.git
cd 仓库名

# 把本包 5 个文件放进目录后：
git add index.html manifest.json sw.js robots.txt README.md
git commit -m "Deploy A330 quiz"
git push origin main
```

然后重复 **方法 A** 的 Settings → Pages 步骤。

### 添加到 iPhone / iPad 主屏幕

1. Safari 打开 GitHub Pages 网址。
2. 输入口令 `1009`。
3. 点分享 → **添加到主屏幕**。  
   （会用到 `manifest.json` 里的名称「A330 题库5389题」）

## 换设备同步错题

App 内点右上角 **同步**：

- **分享/导出** 或 **复制到剪贴板**
- 另一台设备选 **合并导入**（保留两边）或 **覆盖导入**（以这份为准）

## 注意

- 口令只能挡住随便打开的人，不是真正的账号安全。
- 仓库若设为 **Public**，知道网址的人也能访问（仍需口令）。不想公开就设为 **Private**，并用 GitHub Pages 的私有仓库权限（需相应 GitHub 方案）或改用仅自己知道的托管方式。
