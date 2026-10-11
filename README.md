# GitHub Pages 根站点交接

仅发布本目录的 `app-ads.txt`、`index.html`、`.nojekyll` 到 **DBCooperK/dbcooperk.github.io** 仓库根目录。原 `sudoku-pages` 仓库和隐私网址保持不变。无需后端或收费服务器。

1. 登录 GitHub，打开 https://github.com/new ，Owner 选 DBCooperK，Repository name 填 `dbcooperk.github.io`，选 Public。若已经存在则直接打开已有仓库。
2. 点击 Create repository。首次可添加 README，方便直接上传文件。
3. 仓库 Code → Add file → Upload files，上传此目录的 `app-ads.txt`、`index.html`、`.nojekyll` 三个文件（不要上传整个文件夹）。Mac Finder 若看不到 `.nojekyll`，按 Command + Shift + . 显示隐藏文件。点击 Commit changes。
4. Settings → Pages → Build and deployment → Source 选 Deploy from a branch，Branch 选 main、目录选 / (root)，点击 Save。
5. 等待 Pages 构建完成，打开 https://dbcooperk.github.io/app-ads.txt ，确认只显示下面一行：

```text
google.com, pub-8836260304454968, DIRECT, f08c47fec0942fa0
```

6. Google Play Console → 当前应用 → 商店设置（Store settings）→ 商店详情联系信息（Store listing contact details）：网站填 `https://dbcooperk.github.io/`。隐私政策 URL 仍填 `https://dbcooperk.github.io/sudoku-pages/`。
7. AdMob → 应用 → 查看所有应用 → app-ads.txt，使用“检查更新”或对应刷新入口，等待验证。Google 抓取可能延迟，不能把 GitHub 发布成功当作 AdMob 已验证。

不要把 app-ads.txt 仅放在 `/sudoku-pages/` 路径。Google 从商店开发者网站的主机名根目录查找文件。

当前游戏包仍使用测试广告；本次静态文件发布不改变广告模式。官方参考：https://support.google.com/admob/answer/9363762 。
