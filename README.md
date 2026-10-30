# 大雨落下时

原生 HTML、CSS、JavaScript 编写的单文件捡手机剧情模拟器。页面入口为 `index.html`，没有框架或远程资源依赖。已提供的壁纸和头像保存在同仓库的 `assets/`，发布时须连同该目录一起上传。

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


## 界面与备忘录时间线

当前界面版本：`20261030-r3`，可在手机的“设置”页面底部核对。若浏览器保留了旧页面，可打开 `https://kikiyang14-byte.github.io/found-phone-simulator/?v=20261030-r3`；该参数不会清除同一站点的 localStorage 进度。头像和壁纸路径带版本查询参数，替换后可同步更新该参数。

- `assets.avatars.shin` 对应 IMG_9118；`assets.avatars.self` 对应 IMG_9123。列表、对话和资料页复用同一字段，缺图回退首字头像。
- `notes[].timelineOrder` 为相对事件顺序，数字越大越晚；`notes[].group` 与 `interface.noteGroups` 控制原生备忘录分组。`notes[].date` 是展示标签。
- `datePrecision: "stage"` 表示只确定阶段，不是精确年月日；`eventDate` 只用于已有日期锚点。不要通过把相对排序键转换为日期来编造时间。
- 最新两篇按同一录制日 D5（2033-06-06）展示：X-room 在先，雨天约会和当晚短信在后。生日备忘录保留 2026-10-02；2029 年冬天的赴英安排保留该季节锚点。其余按既有事件链排列，不把“夏季学期结束的秘密回国”硬套为旧聊天编排的 12 月。
- 标题、正文、换行、聊天日期和稳定 ID 保持原样。备忘录界面将既有 `□` 行渲染为不可勾选的清单；不会让玩家改写人物内容。

主屏天气小组件未连接外部天气服务；相册小组件只展示已经提供的壁纸图片，不为剧情新增照片。锁屏手电筒入口提供屏幕照明页面，不调用真实手机闪光灯。
