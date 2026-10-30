# 大雨落下时

原生 HTML、CSS、JavaScript 编写的单文件捡手机剧情模拟器。页面入口为 `index.html`，没有外部资源依赖。

## GitHub Pages 发布

在仓库的 **Settings → Pages → Build and deployment** 中设置：

- Source：**Deploy from a branch**
- Branch：**main**
- Folder：**/ (root)**

点击 **Save**。首次发布完成后，在 Pages 设置页查看实际网址。默认项目网址为：

https://kikiyang14-byte.github.io/found-phone-simulator/

提交源文件不等于 Pages 已开启；以设置页的发布状态和实际网址响应为准。

## 更新内容

修改 `index.html` 顶部的 `CONFIG`，检查后提交到 `main`，GitHub Pages 会自动重新发布，网址保持不变。首次开启 Pages 之前不会自动上线。

人物在 `contacts`，聊天在 `chats[].messages`，文字照片在 `photos`，备忘录在 `notes`，通话在 `calls`，通知在 `notifications`，线索在 `clues`。`source` 供作者核对来源，不显示在聊天气泡中。

已确认：李炅潣生日及正式告白为 2026 年 10 月 2 日，申惟旧聊天第 041—048 条为 2026 年 10 月 3 日。

探索进度保存在当前浏览器的 localStorage 中，不会跨手机或浏览器自动同步。保持 `storageKey` 不变可保留更新前的进度；需要重新体验时可在探索进度页重置。
