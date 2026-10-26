# Promoter Rating - GitHub Pages

这是一个无构建步骤、无外部依赖的静态原型。index.html 就是 GitHub Pages 的发布入口。

竖版移动端原型入口为 portrait.html，适用于游戏内竖屏 WebView。

## 部署

建议使用 GitHub Actions 自动发布：新建一个空的 GitHub 仓库后，将本目录内的全部文件（包括 .github 目录）上传到仓库根目录，并推送到 main 分支。然后在仓库的 **Settings** -> **Pages** 中，将 Source 设为 **GitHub Actions**。每次推送 main 分支，站点都会自动更新。

也可以使用 GitHub 的分支发布：

1. 在 GitHub 新建仓库，或将本目录的所有文件上传至现有仓库的根目录。
2. 打开仓库的 **Settings** -> **Pages**。
3. 在 **Build and deployment** 中选择 **Deploy from a branch**。
4. 选择要发布的分支（通常为 main），目录选择 **/(root)**，然后保存。
5. GitHub 完成发布后，在 Pages 页面打开生成的站点链接。

若希望与仓库内其他内容分开管理，可单独新建一个仓库后，上传本目录中的 index.html、.nojekyll 和本说明文件。

## 使用

- 默认进入待评价列表。
- 可通过页面交互切换待评价、已评价、填写详情和游戏内弹窗预览。
- 也可在部署地址末尾添加查询参数直接打开指定视图，例如：
  - ?screen=pending
  - ?screen=reviewed
  - ?screen=game
  - ?screen=native

所有状态仅在浏览器当前页面内演示，刷新页面会恢复初始样例数据。

## 竖版原型

打开 portrait.html 可查看为竖屏 WebView 单独设计的评价流程。它使用单列任务卡、底部固定提交操作与安全区间距，不复用横屏版的侧栏布局。
