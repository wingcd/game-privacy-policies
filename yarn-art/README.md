# 《连线成画》（Yarn Art: Connect & Color）

平台提审材料：隐私政策页面。游戏为毛线绕线填色（钉线画）休闲益智手游。

## 文件说明

- `index.html` — 隐私政策页面（中英俄三语，单文件自包含），手机/桌面自适应，默认按浏览器语言显示，顶部可手动切换；支持 `?lang=zh` / `?lang=en` / `?lang=ru` 参数固定语言

## 在线地址

部署在本仓库的 GitHub Pages 上：

- https://wingcd.github.io/game-privacy-policies/yarn-art/

平台后台需要填 URL 时直接用上面的地址（俄语区可用 `?lang=ru` 后缀）。

## 基本信息

| 项 | 值 |
| --- | --- |
| 中文名 | 连线成画（已确认正式名，见项目 `docs/连线成画-多语言名称与商店描述.md`） |
| 英文名 | Yarn Art: Connect & Color |
| 俄文名 | Картины из пряжи |
| 项目路径 | H:\game_dev\毛线填色\project（Cocos Creator 3.8 工程，项目名 thread-jam） |
| 平台 | 微信 / 抖音 / 快手 / 支付宝 / 美团 / TapTap 等小游戏渠道 + Google Play（buildconfigs 含 wechatgame、tt、ks、alipay、meituan、taptap、gp.yalle 等） |
| 类型 | 休闲益智 · 毛线绕线填色 |
| 上架文案 | 项目内 `docs/连线成画-多语言名称与商店描述.md` |
| 开发主体 | 成都致样互动科技有限公司 |
| 联系邮箱 | wingcd@foxmail.com |

## 政策内容与实际代码核对（2026-10-28）

- **平台账号标识**：宿主应用登录换取用户 ID（`zysdk/user.ts` login 流程）；
- **昵称/头像**：排行榜展示用到 `nickName / avatarUrl`（`zysdk/leaderboard.ts`，游戏内有 `ButtonRank` / `ButtonFriendRank` 全球+好友排行榜），政策含"用户信息（昵称、头像）"条款，仅限排行榜展示目的；
- **云端存档**：游戏进度走 `/user/saveData` 同步游戏服务器（`zysdk/user.ts:67`，本地 + 云端双存档），政策含"云端数据"条款；
- **广告**：激励视频（`AdManager.ts` VideoInfo，`AdGetPropWindow` 看广告领道具）+ 横幅（`FailWindow` / `PauseWindow` / `AddToDeskWindow` 等调用 `setBannerAdVisible`）+ 插屏（`showInterstitialAd`），政策按"激励视频广告及横幅、插屏等广告形式"表述；
- **支付**：SUD 道具直购（`zysdk/sud.ts` / `order.ts`，服务端签名发货）及 `yalla_pay.ts`（Google Play 渠道），政策含"支付服务"条款（平台支付，仅接收交易结果）；
- **行为统计**：heartbeat / counter 匿名统计（`zysdk/heartbeat.ts`、`zysdk/counter.ts`），政策含"行为数据"条款；
- **本地数据**：金币、道具、设置存本地，政策"本地数据"条款与之一致。

## 需要注意 / 后续要改的地方

| 位置 | 说明 |
| --- | --- |
| 日期 | 页面顶部「更新日期 / 生效日期」目前是 2026-10-28，政策改版时记得同步 |
| 邮箱 | 目前用 `wingcd@foxmail.com`，如换主体邮箱需全局替换 |
| 俄语 | 游戏本体尚无 ru 资源（工程 i18n 目录的 ar/zhtc 为模板遗留，游戏实际不启用）；上架俄区前需按定名文档落地清单补齐游戏内俄语 |
