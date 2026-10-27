# 《巧手拼豆》（Bead Art Master）

SUD（OpenPaaS）平台提审材料：隐私政策页面。游戏为拼豆（Perler / Fuse Beads）放置解谜手游，全球投放 cn / sea / eu / ru。

## 文件说明

- `index.html` — 隐私政策页面（中英俄三语，单文件自包含），手机/桌面自适应，默认按浏览器语言显示，顶部可手动切换；支持 `?lang=zh` / `?lang=en` / `?lang=ru` 参数固定语言

## 在线地址

部署在本仓库的 GitHub Pages 上：

- https://wingcd.github.io/game-privacy-policies/bead-art-master/

平台后台需要填 URL 时直接用上面的地址（俄语区可用 `?lang=ru` 后缀）。

## 基本信息

| 项 | 值 |
| --- | --- |
| 中文名 | 巧手拼豆 |
| 英文名 | Bead Art Master |
| 俄文名 | Мастер бисера |
| 项目路径 | H:\game_dev\拼豆\project（Cocos Creator 3.8 工程，项目名 thread-jam） |
| 平台 | SUD（OpenPaaS）小游戏，构建配置 buildconfigs/openpass（另有微信/抖音/快手/支付宝/TapTap 等多渠道构建配置） |
| 类型 | 休闲益智 · 拼豆消除 |
| 上架文案 | 项目内 `docs/SUD上架文案-巧手拼豆.md` |
| 开发主体 | 成都致样互动科技有限公司 |
| 联系邮箱 | wingcd@foxmail.com |

## 政策内容与实际代码核对（2026-10-27）

- **平台账号标识**：宿主应用登录换取用户 ID（`zysdk/user.ts` login 流程，`SudAdapter` 提供 `sud.login`）；
- **昵称/头像**：排行榜展示用到 `UserModel.nickName / avatarUrl`（`RankWindow.ts` / `RankItemView.ts`，`zysdk/leaderboard.ts`），政策含"用户信息（昵称、头像）"条款，仅限排行榜展示目的；
- **云端存档**：游戏进度走游戏服务器存档（本地 + 云端双存档，`BaseDAO.ts` + zysdk），政策含"云端数据"条款；
- **广告**：激励视频（`SudAdapter` `createRewardedVideoAd`，另有插屏/横幅），政策按"激励视频广告（补充道具、获取额外奖励等场景）"表述；
- **支付**：SUD 道具直购（`zysdk/sud.ts` `/sud/order/*`，服务端签名发货），政策含"支付服务"条款（平台支付，仅接收交易结果）；
- **行为统计**：heartbeat / counter 匿名统计（`zysdk/heartbeat.ts`、`zysdk/counter.ts`、`StatisticController.ts`），政策含"行为数据"条款；
- **本地数据**：金币（`UserDAO.ts`）、道具、设置存本地，政策"本地数据"条款与之一致。

## 需要注意 / 后续要改的地方

| 位置 | 说明 |
| --- | --- |
| 日期 | 页面顶部「更新日期 / 生效日期」目前是 2026-10-27，政策改版时记得同步 |
| 邮箱 | 目前用 `wingcd@foxmail.com`，如换主体邮箱需全局替换 |
| 游戏名 | 英文名 Bead Art Master、俄文名 Мастер бисера 取自 `docs/SUD上架文案-巧手拼豆.md`；如最终定名不同（备选 Bead Art: Pixel Puzzle 等），需同步改页面标题、语言切换文案与本 README |
